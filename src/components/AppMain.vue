<script>
import Pages from './Pages.vue';
import Portfolio from './Portfolio.vue';
import Blog from './Blog.vue';
import Shop from './Shop.vue';
import Elements from './Elements.vue';

export default {
    name: 'AppMain',

    components: {
        Pages,
        Portfolio,
        Blog,
        Shop,
        Elements 
    }
}

</script>

<template>
  <Pages></Pages>
  <Portfolio></Portfolio>
  <Blog></Blog>
  <Shop></Shop>
  <Elements></Elements>
</template>

<style lang="scss" scoped>
    
</style>
