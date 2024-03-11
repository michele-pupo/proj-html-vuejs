<script>
export default {
    name: 'ElementsImageItem',

    props:{
        image: String,
        name: String, 
        text: String,
        signature: String,
        number: Number,
        date: String
    }
}

</script>

<template>
   <div id="single-image">
        <img :src="image" :alt="name">
        <h3>{{ text }}</h3>
        <h4>{{ signature }}</h4>
        <div id="date">
            <h5>{{ number }}</h5>
            <h6>{{ date }}</h6>
        </div>
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