<script>
import ElementsImageItem from './ElementsImageItem.vue';

export default {
    name: 'Elements',

    components:{ElementsImageItem},

    data() {
        return {
            images:[
                {
                    "thumb": "../../public/img/h-2-blog-img-1.jpg",
                    "name": "h-2-blog-img-1",
                    "text": "This way, loves: a detail guide trough new design",
                    "signature": "By Emily Fields",
                    "number": "07",
                    "date": "May '19"
                },
                {
                    "thumb": "../../public/img/h-2-blog-img-2.jpg",
                    "name": "h-2-blog-img-2",
                    "text": "I try to give people a different way of looking art",
                    "signature": "By Emily Fields",
                    "number": "07",
                    "date": "May '19"
                },
                {
                    "thumb": "../../public/img/h-2-blog-img-3.jpg",
                    "name": "h-2-blog-img-3",
                    "text": "Introduce Richard Laperrière of those amazing features",
                    "signature": "By Emily Fields",
                    "number": "07",
                    "date": "May '19"
                },
            ]
        }
    },
}
</script>

<template>
    <div id="container">
        <div id="image-list">
            <ElementsImageItem
                v-for="currentImage in images"
                :image="currentImage.thumb"
                :name="currentImage.name"
                :text="currentImage.text"
                :signature="currentImage.signature"
                :number="currentImage.number"
                :date="currentImage.date">
            </ElementsImageItem>
        </div>
        <div id="top">
            <img src="../../public/img/svg-2.svg" alt="">
        </div>
    </div>

</template>

<style lang="scss" scoped>
@use '../styles/_variables' as *;

    #container{
        position: relative;
        height: 710px;

        #image-list{
            width: 1300px;
            margin: 0px auto;
            display: flex;
            gap: 30px;
            padding: 150px 0px 10px 0px;
        }

        #top{
            width: 30px;

            img{
                background-color: $primary-color;
                position: absolute;
                top: 30px;
                right: 20px;
                padding: 10px;
                &:hover{
                    opacity: 0.6;
                    cursor: pointer;
                }
            }
        }
    }
    
</style>