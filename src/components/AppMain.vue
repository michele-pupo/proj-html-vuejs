<script>
import Portfolio from './Portfolio.vue';
import Blog from './Blog.vue';
import Shop from './Shop.vue';

export default {
    name: 'AppMain',

    components: {
        Portfolio,
        Blog,
        Shop
    }
}

</script>

<template>
  <Portfolio></Portfolio>
  <Blog></Blog>
  <Shop></Shop>
</template>

<style lang="scss" scoped>
    
</style>
