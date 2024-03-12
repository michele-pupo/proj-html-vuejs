<script>
export default {
    name: 'Blog',
}

</script>

<template>
    <div id="container">
        <div id="blog">
            <div id="blog-title">
                <h2 class="text-center">Working <i>process</i></h2>
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
        <div id="top">
            <img src="../../public/svg/svg-2.svg" alt="">
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/_variables' as *;

    #container{
        position: relative;

        #blog{
            height: 550px;

            #blog-title{

                h2{
                    font-size: 50px;
                }

                i{
                    font-weight: bold;
                }
            }
        
            #blog-icons{
                max-width: 1300px;
                margin: 0 auto;
                display: flex;
                gap: 30px;
                background-image: url(../../public/svg/svg-3.svg);
                background-size: 85%;
                background-repeat: no-repeat;
                background-position: 50% 40%;

                #icons{
                    width: calc(100% / 4);
                    padding-top: 90px;
                    
                    #icon{
                        margin-left: 80px;
                        margin-bottom: 30px;
                        max-width: 150px;
                        height: 150px;
                        background-color: $fourth-color;
                        display: flex;
                        align-items: center;
                        justify-content: center;
                        border-radius: 50%;

                            i{
                                font-size: 40px;
                            }

                            .fa-lightbulb{
                                color: $color-icon-1;
                            }

                            .fa-comment{
                                color: $color-icon-2;
                            }

                            .fa-cloud{
                                color: $color-icon-3;
                            }

                            .fa-pen-clip{
                                color: $color-icon-4;
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
        }

        #top{
            width: 30px;

            img{
                background-color: $primary-color;
                position: absolute;
                bottom: 30px;
                right: 20px;
                padding: 10px;
            }
        }
    }
</style>
