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
            <button>
                Read more
            </button>
        </div>
        <div id="carousel">
           <Slider></Slider>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    #pages{
        margin: 0 auto;
        height: 630px;
        display: flex;
        justify-content: space-evenly;
        align-items: center;

        #title{
            padding: 100px 0px;
            max-width: 700px;
            z-index: 0;

            h1{
                font-size: 85px;
            }

            p{
                font-size: 22px;
            }
        }
    }
</style>