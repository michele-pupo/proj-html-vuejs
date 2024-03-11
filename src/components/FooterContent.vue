<script>
import LogoItem from './LogoItem.vue';

export default {
    name: 'FooterContent',

    components: {
        LogoItem,
    }
}
</script>

<template>
  <div id="container-footer">
    <div id="logo">
        <LogoItem></LogoItem>
        <h6>Let's Get Creative</h6>
    </div>
    <div id="email">
        <h6>maree.qode@gmail.com</h6>
        <h6>+44645 321 789</h6>
    </div>
    <div id="address">
        <h6>Avenue d'Auderghem 10</h6>
        <h6>1040 Brussels, Belgium</h6>
    </div>
    <div id="touch">
        <h6>Stay in touch with us</h6>
        <div id="social">
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-pinterest-p"></i>
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-linkedin-in"></i>
        </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
    #container-footer{
        max-width: 1300px;
        margin: 0 auto;
        padding: 70px 0px;
        display: flex;
        justify-content: space-between;

        h6{
            font-size: 15px;
            padding-top: 10px;
        }

        #touch{
            #social{
                padding-top: 10px;
                display: flex;
                gap: 30px;
            }
        }
    }
</style>