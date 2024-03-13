<script>
export default {
    name: 'Shop',

}

</script>

<template>
    <div id="shop">
        <div id="shop-text">
            <h2>Want to work with us? Send us <i>a message!</i></h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do aiusmod tempor incididunt ut labore et dolore. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea comma.</p>
        </div>
        <div id="button">
            <button>Contact</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/_variables' as *;

    #shop{
        height: 450px;
        background-image: url(../../public/img/h-2-background-1.jpg);
        background-position: 0% 30%;
        background-repeat: no-repeat;
        background-size: cover;

        #shop-text{
            max-width: 1400px;
            margin: 0 auto;
            padding-top: 130px;
            text-align: center;

            h2{
                font-size: 70px;
                padding-bottom: 20px;
                font-weight: 300;

                i{
                    font-family: 'Playball', sans-serif;
                    font-size: 90px;
                }
            }

            p{
                font-size: 19px;
                color: $text-color-secondary;
            }
        }

        #button{
            display: flex;
            justify-content: center;
            margin-top: 30px;
            
            button{
                background-color: $bg-button-1;
                padding: 10px 50px;
                border-color: transparent;
                color: #000000;
                font-size: 12px;
                text-transform: uppercase;
                font-weight: bold;
                &:hover{
                    background-color: $secondary-color;
                }
            }
        }
    }
</style>