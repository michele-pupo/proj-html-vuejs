<script>
import ImageItem from './ImageItem.vue';

export default {
    name: 'MainImage',

    components:{ImageItem},

    data() {
        return {
            images:[
                {
                    "thumb": "../../public/img/h-2-port-img-1.jpg"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-2.jpg"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-3.jpg"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-4.jpg"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-5.jpg"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-6.jpg"
                }
            ]
        }
    },

};
</script>

<template>
    <div id="images-list">
        <ImageItem
            v-for="currentImage in images"
            :image="currentImage.thumb">
        </ImageItem>
    </div>
</template>

<style lang="scss" scoped>
    #images-list{
        display: flex;
        flex-flow: row wrap;
    }
</style>