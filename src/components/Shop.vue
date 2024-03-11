<script>
export default {
    name: 'Shop',

}

</script>

<template>
    <div id="shop">
        <div id="shop-text">
            <h2>Want to work with us? Send us <i>a message!</i></h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt repudiandae ex, dolores doloribus, adipisci corrupti mollitia nulla quae, hic voluptatum dolorum debitis quis reiciendis repellendus enim. Voluptatem nisi corporis dolor.</p>
        </div>
        <div id="button">
            <button>Contact</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    #shop{
        height: 450px;
        background-image: url(../../public/img/h-2-background-1.jpg);
        background-position: 0% 25%;
        background-repeat: no-repeat;
        background-size: cover;

        #shop-text{
            max-width: 1400px;
            margin: 0 auto;
            padding-top: 170px;
            text-align: center;

            h2{
                font-size: 50px;
                padding-bottom: 30px;

                i{
                    font-weight: bold;
                }
            }

            p{
                font-size: 15px;
            }
        }

        #button{
            display: flex;
            justify-content: center;
            margin-top: 30px;
            
            button{
                background-color: #d8f0e3;
                padding: 5px 50px;
                border-color: transparent;
                color: black;
                font-size: 12px;
            }
        }
    }
</style>