<script>
import PortfolioImageItem from './PortfolioImageItem.vue';

export default {
    name: 'Portfolio',

    components:{PortfolioImageItem},

    data() {
        return {
            images:[
                {
                    "thumb": "../../public/img/h-2-port-img-1.jpg",
                    "name": "h-2-port-img-1"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-2.jpg",
                    "name": "h-2-port-img-2"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-3.jpg",
                    "name": "h-2-port-img-3"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-4.jpg",
                    "name": "h-2-port-img-4"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-5.jpg",
                    "name": "h-2-port-img-5"
                },
                {
                    "thumb": "../../public/img/h-2-port-img-6.jpg",
                    "name": "h-2-port-img-6"
                }
            ]
        }
    },

};
</script>

<template>
    <div id="images-list">
        <PortfolioImageItem
            v-for="currentImage in images"
            :image="currentImage.thumb"
            :name="currentImage.name">
        </PortfolioImageItem>
    </div>
</template>

<style lang="scss" scoped>
    #images-list{
        display: flex;
        flex-flow: row wrap;
    }
</style>./PortfolioImageItem.vue