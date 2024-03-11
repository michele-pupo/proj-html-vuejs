<script>
export default {
    name: 'ImageItem',

    props:{
        image: String,
    }
};
</script>

<template>
    <div id="single-image">
        <img :src="image" alt="">
    </div>
</template>

<style lang="scss" scoped>
    #single-image{
        width: calc(100% / 3);

        img{
            width: 100%;
        }
    }
</style>