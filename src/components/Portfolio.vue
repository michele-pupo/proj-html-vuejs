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
                    "name": "h-2-port-img-4",
                    "titleoverlay": "Illustrations of novels",
                    "textoverlay": "Illustration"
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
    <div id="container">
        <div id="images-list">
            <PortfolioImageItem
                v-for="currentImage in images"
                :image="currentImage.thumb"
                :name="currentImage.name"
                :titleoverlay="currentImage.titleoverlay"
                :textoverlay="currentImage.textoverlay">
            </PortfolioImageItem>
        </div>
        <div id="top">
            <img src="../../public/img/svg-2.svg" alt="">
        </div>
        <div id="top-2">
            <img src="../../public/img/svg-2.svg" alt="">
        </div>
        <div id="cart">
            <img src="../../public/img/svg-6.svg" alt="">
        </div>
        <div id="logo">
            <img src="../../public/img/svg-4.svg" alt="">
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/_variables' as *;

    #container{
        position: relative;

        #images-list{
            display: flex;
            flex-flow: row wrap;
        }

        #top{
            width: 30px;

            img{
                background-color: $primary-color;
                position: absolute;
                bottom: 180px;
                right: 20px;
                padding: 10px;
                &:hover{
                    opacity: 0.6;
                    cursor: pointer;
                }
            }
        }

        #top-2{
            width: 30px;

            img{
                background-color: $primary-color;
                position: absolute;
                bottom: 1050px;
                right: 20px;
                padding: 10px;
                &:hover{
                    opacity: 0.6;
                    cursor: pointer;
                }
            }
        }

        #cart{
            width: 30px;

            img{
                background-color: $bg-img-1;
                width: 45px;
                position: absolute;
                top: 210px;
                right: 0;
                padding: 10px;
                &:hover{
                    opacity: 0.6;
                    cursor: pointer;
                }
            }
        }

        #logo{
            width: 30px;

            img{
                background-color: $bg-img-2;
                width: 45px;
                position: absolute;
                top: 150px;
                right: 0;
                padding: 10px;
                &:hover{
                    opacity: 0.6;
                    cursor: pointer;
                }
            }
        }
    }
</style>