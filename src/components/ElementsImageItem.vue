<script>
export default {
    name: 'ElementsImageItem',

    props:{
        image: String,
        name: String, 
        text: String,
        signature: String,
        number: String,
        date: String
    }
}

</script>

<template>
   <div id="single-image">
        <img :src="image" :alt="name">
        <div id="text">
            <h3>{{ text }}</h3>
            <h4><i>{{ signature }}</i></h4>
        </div>
        <div id="date">
            <div id="day">
                <h5>{{ number }}</h5>
            </div>
            <div id="month-container">
                <div id="month">
                    <h6>{{ date }}</h6>
                </div>
            </div>
        </div>
   </div>
</template>

<style lang="scss" scoped>
@use '../styles/_variables' as *;

    #single-image{
        width: calc(100% / 3);

        img{
            width: 100%;
        }

        #text{
            margin-top: 35px;

            h3{
                font-size: 28px;
            }

            h4{
                font-size: 15px;
                margin-top: 20px;
            }
        }

        #date{
            position: relative;
            top: -465px;
            right: -20px;
            display: flex;
            flex-direction: column;

            #day{
                background-color: $primary-color;
                width: 80px;
                height: 50px;
                padding-top: 8px;
                display: flex;
                align-items: center;
                justify-content: center;
                
                h5{
                    font-size: 40px;
                    font-family: 'Playball', sans-serif;
                }
            }

            #month-container{
                width: 97px;
                height: 100px;
                text-align: center;
                overflow: hidden;
                position: relative;

                #month{
                    width: 120%; 
                    height: 50%; 
                    background-color: $terziary-color;
                    padding-top: 5px;
                    position: absolute; 
                    bottom: 40; 
                    right: 0; 
                    clip-path: polygon(15% 0%, 85% 0%, 85% 80%, 50% 60%, 15% 80%);

                    h6{
                        font-weight: bold;
                        font-size: 15px;
                    }
                }
            }
        }
    }
</style>