<script>
export default {
    name: 'ListLinks',

    data() {
        return {
            links: [
                'Home',
                'Pages',
                'Portfolio',
                'Blog',
                'Shop',
                'Elements'
            ]
        }
    },
};
</script>

<template>
    <div class="d-flex align-items-center gap-5">
        <ul class="d-flex list-unstyled pt-3 gap-5">
            <li v-for="currentLink in links">
                <a href="#">{{ currentLink }}</a>
            </li>
        </ul>
        <img src="../../public/svg/svg-1.svg" alt="">
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/_variables' as *;

    a{
        color: black;
        text-decoration: none;

        &:hover{
            border-bottom: 8px solid $border-color;
            padding-bottom: 5px;
        }
    }
</style>