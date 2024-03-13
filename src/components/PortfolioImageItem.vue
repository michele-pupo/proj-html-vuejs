<script>
export default {
    name: 'PortfolioImageItem',

    props:{
        image: String,
        name: String,
        titleoverlay: String,
        textoverlay: String
    }
};
</script>

<template>
    <div id="single-image">
        <img :src="image" :alt="name" class="portfolio-image">
        <div v-if="titleoverlay && textoverlay" id="text">
            <h3> {{ titleoverlay }} </h3>
            <h4><i>{{ textoverlay }}</i></h4>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    #single-image{
        width: calc(100% / 3);

        img{
            width: 100%;
            cursor: pointer;
        }

        .portfolio-image {
            width: 100%;
            transition: opacity 0.3s, filter 0.3s;

            &:hover{
                opacity: 0.5;
                filter: brightness(0.8); 
            }
        }

        #text{
            background-image: url(../../public/img/rbt-placeholder.jpg);
            width: 380px;
            height: 150px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            position: relative;
            top: -530px;
            padding-left: 50px;
            visibility: hidden;
            opacity: 0;
            transition: opacity 0.3s;

            h3{
                font-size: 30px;
            }
        }

        &:hover #text{
            visibility: visible;
            opacity: 1;
        }
    }
</style>