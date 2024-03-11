<script>
import LogoItem from './LogoItem.vue';
import ListLinks from './ListLinks.vue';

export default {
    name: 'AppHeader',

    components: {
        LogoItem,
        ListLinks
    }
}

</script>

<template>
    <div id="logo-links" class="d-flex align-items-center justify-content-between px-5 ">
        <LogoItem></LogoItem>
        <ListLinks></ListLinks>
    </div>
</template>

<style lang="scss" scoped>
    #logo-links{
        height: 100px;
    }
</style>
