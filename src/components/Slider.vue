<script>
import SliderImageItem from './SliderImageItem.vue';

export default {
    name: 'Slider',

    components: {SliderImageItem},

    data() {
        return {
            images: [
                {
                    "imageprincipal1": "../../public/img/h-2-slider-img-15.png",
                    "imageprincipal2": "../../public/img/h-2-slider-img-16.png",
                    "flower1": "../../public/img/h-2-slider-img-12.png",
                    "flower2": "../../public/img/h-2-slider-img-13.png",
                    "flower3": "../../public/img/h-2-slider-img-14.png",
                    "flower4": "../../public/img/h-2-slider-img-17.png",
                    "flower5": "../../public/img/short-slider-rev-1-img-2.png",
                    "flower6": "../../public/img/short-slider-rev-1-img-6.png"
                },
                {
                    "imageprincipal1": "../../public/img/h-2-slider-img-11.png",
                    "flower1": "../../public/img/h-2-slider-img-13.png",
                    "flower2": "../../public/img/h-2-slider-img-12.png",
                    "flower3": "../../public/img/short-slider-rev-1-img-6.png",
                    "flower4": "../../public/img/h-2-slider-img-17.png",
                    "flower5": "../../public/img/short-slider-rev-1-img-2.png",
                    "flower6": "../../public/img/short-slider-rev-1-img-10.png"
                },
                {
                    "imageprincipal1": "../../public/img/short-slider-rev-1-img-3.png",
                    "flower1": "../../public/img/h-2-slider-img-17.png",
                    "flower2": "../../public/img/short-slider-rev-1-img-10.png",
                    "flower3": "../../public/img/h-2-slider-img-12.png",
                    "flower4": "../../public/img/short-slider-rev-1-img-6.png",
                    "flower5": "../../public/img/short-slider-rev-1-img-4.png",
                    "flower6": "../../public/img/short-slider-rev-1-img-6.png"
                }
            ]
        };
    }
}
</script>

<template>
    <div>
        <SliderImageItem :images="images"></SliderImageItem>
    </div>
  </template>

<style lang="scss" scoped>
    
</style>