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
        },

        goToSlide(index) {
            this.currentIndex = index;
        }
    }
}
</script>

<template>
    <div class="slider">
        <button class="prev" @click="prev" :disabled="currentIndex === 0">Prev</button>
        <div class="slides">
            <div v-for="(image, index) in images" :key="index" class="slide" v-show="index === currentIndex">
                <div class="image-slide-container">
                    <img id="principal1" :src="image.imageprincipal1" alt="">
                    <img id="principal2" :src="image.imageprincipal2" alt="">
                    <img id="flower1" :src="image.flower1" alt="">
                    <img id="flower2" :src="image.flower2" alt="">
                    <img id="flower3" :src="image.flower3" alt="">
                    <img id="flower4" :src="image.flower4" alt="">
                </div>
            </div>
        </div>
        <button class="next" id="next" @click="next" :disabled="currentIndex === images.length - 1">Next</button>
        <div class="pagination">
            <span
                    v-for="(image, index) in images"
                    :key="index"
                    class="dot"
                    :class="{ active: index === currentIndex }"
                    @click="goToSlide(index)">
            </span>
        </div>
    </div>
</template>
  
<style lang="scss" scoped>
    .slider {
        display: flex;
        align-items: center;
        width: 600px;

        button{
            z-index: 10;
            position: relative;
        }

        .prev{
            right: 1000px;
        }

        .next{
            left: 200px;
        }

        .slides {
            flex: 1;
            overflow: hidden;

            .slide {
                width: 100%;
                transition: opacity 0.5s ease;

                .image-slide-container{
                    display: flex;
                    position: absolute;
                    top: 130px;
                    right: 1px;
                    z-index: 0;

                    #principal1{
                         width: 100%;
                         padding-left: 20px;
                    }

                    #flower1, #flower2, #flower3, #flower4{
                        width: 100%;
                        height: 100%;
                        position: relative;
                    }

                    #flower1{
                        right: 740px;
                        top: 200px;
                    }

                    #flower2{
                        right: 760px;
                        top: 350px;
                    }

                    #flower3{
                        right: 200px;
                        top: 0px;
                    }

                    #flower4{
                        right: 200px;
                        top: 300px;
                    }
                }
            }
        }
    }

    button {
        margin: 0 10px;
    }

    .pagination {
        display: flex;
        justify-content: center;
        margin-top: 10px;

        .dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background-color: #bbb;
            margin: 0 5px;
            cursor: pointer;

            &.active{
                background-color: #333;
            }
        }
    }
</style>