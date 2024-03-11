<script>
export default {
    name: 'Blog',

}

</script>

<template>
    <div id="blog">
        <div id="blog-title">
            <h2 class="text-center pt-5">Working <i>process</i></h2>
        </div>
        <div id="blog-icons">
            <div id="icons">
                <div id="icon">
                    <i class="fa-solid fa-lightbulb"></i>
                </div>
                <div id="icon-text">
                    <h3>First theres an idea</h3>
                    <p>Lorem ipsum dolor sit, conetu adipisisc sed be et are aliqua please itself.</p>
                </div>
            </div>
            <div id="icons">
                <div id="icon">
                    <i class="fa-regular fa-comment"></i>
                </div>
                <div id="icon-text">
                    <h3>Then we talk about</h3>
                    <p>Lorem ipsum dolor sit, conetu adipisisc sed be et are aliqua please itself.</p>
                </div>
            </div>
            <div id="icons">
                <div id="icon">
                    <i class="fa-solid fa-cloud"></i>
                </div>
                <div id="icon-text">
                    <h3>And we think about</h3>
                    <p>Lorem ipsum dolor sit, conetu adipisisc sed be et are aliqua please itself.</p>
                </div>
            </div>
            <div id="icons">
                <div id="icon">
                    <i class="fa-solid fa-pen-clip"></i>
                </div>
                <div id="icon-text">
                    <h3>So we draw along</h3>
                    <p>Lorem ipsum dolor sit, conetu adipisisc sed be et are aliqua please itself.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    #blog{
        height: 710px;

        i{
            font-weight: bold;
        }

        img{
            background-color: red;
        }
    }

    #blog-icons{
        max-width: 1300px;
        margin: 0 auto;
        display: flex;
        gap: 30px;

        #icons{
        width: calc(100% / 4);
        padding-top: 90px;
        
            #icon{
                margin-left: 90px;
                margin-bottom: 30px;
                max-width: 130px;
                height: 130px;
                background-color: #faf7f1;
                display: flex;
                align-items: center;
                justify-content: center;
                border-radius: 50%;

                    i{
                        font-size: 35px;
                    }

                    .fa-lightbulb{
                        color: #BADAC9;
                    }

                    .fa-comment{
                        color: #f8d12d;
                    }

                    .fa-cloud{
                        color: #80465f;
                    }

                    .fa-pen-clip{
                        color: #f0817b;
                    }
            }

            #icon-text{
                text-align: center;

                h3{
                    font-size: 20px;
                }

                p{
                    font-size: 15px;
                }
            }
        }
    }
    
</style>
