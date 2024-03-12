<script>
import FooterContent from './FooterContent.vue';

export default {
    name: 'AppFooter',

    components: {
        FooterContent,
    }
}
</script>

<template>
  <div id="footer">
    <FooterContent></FooterContent>
  </div>
</template>

<style lang="scss" scoped>
@use '../styles/_variables' as *;

    #footer{
        height: 230px;
        background-color: $primary-color;
    }
</style>
