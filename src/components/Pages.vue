<script>
import Slider from './Slider.vue';

export default {
    name: 'Pages',

    components:{Slider}
}
</script>

<template>
    <div id="pages">
        <div id="title">
            <h1>
                Devotion that never <i>ends</i>
            </h1>
            <p>
                Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consecteur, adipisci velit, sed quia non numquam eius modi.
            </p>
            <button id="more">
                Read more
            </button>
        </div>
        <div id="carousel">
           <Slider></Slider>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/_variables' as *;

    #pages{
        margin: 0 auto;
        height: 700px;
        display: flex;
        justify-content: space-evenly;
        align-items: center;

        #title{
            max-width: 700px;

            h1{
                font-size: 85px;
                font-weight: 300;
                line-height: 1;

                i{
                    font-family: 'Playball', sans-serif;
                    font-size: 110px;
                }
            }

            p{
                font-size: 22px;
                color: $text-color-secondary;
            }

            #more{
                background-color: transparent;
                border: 3px solid $secondary-color;
                color: #000000;
                font-size: 13px;
                font-weight: bold;
                text-transform: uppercase;
                padding: 15px 40px;
                margin-top: 20px;

                &:hover{
                    background-color: $secondary-color;
                }
            }
        }
    }
</style>