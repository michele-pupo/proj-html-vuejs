<script>
import SliderImageItem from './SliderImageItem.vue';

export default {
    name: 'Slider',

    components: {SliderImageItem},

    data() {
        return {
            images: [
                {
                    "thumb": "../../public/img/h-2-slider-img-15.png",
                },
                {
                    "thumb": "../../public/img/h-2-slider-img-16.png",
                },
                {
                    "thumb": "../../public/img/h-2-slider-img-17.png",
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