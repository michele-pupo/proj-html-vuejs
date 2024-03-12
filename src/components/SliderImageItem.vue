<script>
export default {
    name: 'SliderImageItem',

    props: {
        images: {
            type: Array,
            required: true
        }
    },

    data() {
        return {
            currentIndex: 0
        };
    },

    methods: {
        next() {
            if (this.currentIndex < this.images.length - 1) {
                this.currentIndex++;
            }
        },

        prev() {
            if (this.currentIndex > 0) {
                this.currentIndex--;
            }
        }
    }
}
</script>

<template>
    <div class="slider">
        <button @click="prev" :disabled="currentIndex === 0">Prev</button>
        <div class="slides">
            <div v-for="(image, index) in images" :key="index" class="slide" v-show="index === currentIndex">
                <img :src="image.thumb" alt="">
            </div>
        </div>
        <button @click="next" :disabled="currentIndex === images.length - 1">Next</button>
    </div>
  </template>
  
<style lang="scss" scoped>
    .slider {
  display: flex;
  align-items: center;
}

.slides {
  flex: 1;
  overflow: hidden;
}

.slide {
  width: 100%;
  transition: opacity 0.5s ease;
}

button {
  margin: 0 10px;
}
</style>