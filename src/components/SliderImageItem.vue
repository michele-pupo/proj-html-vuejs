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
        <button class="prev" @click="prev" :disabled="currentIndex === 0"><i class="fa-solid fa-angle-left"></i></button>
        <div class="slides">
            <div v-for="(image, index) in images" :key="index" class="slide" v-show="index === currentIndex">
                <div class="image-slide-container">
                    <img id="principal1" :src="image.imageprincipal1" alt="">
                    <img id="principal2" :src="image.imageprincipal2" alt="">
                    <img id="flower1" :src="image.flower1" alt="">
                    <img id="flower2" :src="image.flower2" alt="">
                    <img id="flower3" :src="image.flower3" alt="">
                    <img id="flower4" :src="image.flower4" alt="">
                    <img id="flower5" :src="image.flower5" alt="">
                    <img id="flower6" :src="image.flower6" alt="">
                </div>
            </div>
        </div>
        <button class="next" id="next" @click="next" :disabled="currentIndex === images.length - 1"><i class="fa-solid fa-angle-right"></i></button>
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
@use '../styles/_variables' as *;

    .slider {
        display: flex;
        max-width: 1450px;

        button{
            z-index: 10;
            position: relative;
            background-color: $secondary-color;
            border: transparent;
            border-radius: 50%;
            padding: 10px 15px;

            i{
                font-size: 20px;
            }
        }

        .prev{
            right: 1680px;

            &:hover{
                background-color: $terziary-color;
                cursor: pointer;
            }
        }

        .next{
            right: -550px;

            &:hover{
                background-color: $terziary-color;
                cursor: pointer;
            }
        }

        .slides {
            flex: 1;
            overflow: hidden;

            .slide {
                width: 100%;
                transition: opacity 0.8s ease;

                .image-slide-container{
                    display: flex;
                    gap: 20px;
                    position: absolute;
                    top: 180px;
                    right: 50px;
                    z-index: 0;

                    #principal1{
                         width: 100%;
                         position: relative;
                         right: -120px;
                    }

                    #principal2{
                         width: 100%;
                         position: relative;
                         right: -100px;
                    }

                    #flower1, #flower2, #flower3, #flower4, #flower5, #flower6{
                        width: 100%;
                        height: 100%;
                        position: relative;
                    }

                    #flower1{
                        right: 650px;
                        top: 200px;
                    }

                    #flower2{
                        right: 750px;
                        top: 350px;
                    }

                    #flower3{
                        right: 170px;
                        top: -30px;
                    }

                    #flower4{
                        right: 150px;
                        top: 300px;
                    }

                    #flower5{
                        right: 920px;
                        top: -50px;
                    }

                    #flower6{
                        right: 320px;
                        top: 70px;
                    }
                }
            }
        }

        .pagination {
            display: flex;
            justify-content: center;
            margin-top: 10px;

            .dot {
                width: 10px;
                height: 10px;
                border-radius: 50%;
                background-color: $secondary-color;
                margin: 0 10px;
                cursor: pointer;
                z-index: 10;
                position: relative;
                top: 300px;
                right: 750px;

                &.active{
                    width: 13px;
                    height: 13px;
                    background-color: $secondary-color;
                }
            }
        }
    }
</style>