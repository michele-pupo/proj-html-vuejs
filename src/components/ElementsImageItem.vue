<script>
export default {
    name: 'ElementsImageItem',

    props:{
        image: String,
        name: String, 
        text: String,
        signature: String,
        number: Number,
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
            <div id="month">
                <h6>{{ date }}</h6>
            </div>
        </div>
   </div>
</template>

<style lang="scss" scoped>
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
                background-color: #c0e1cf;
                width: 80px;
                height: 50px;
                text-align: center;
                padding-top: 5px;

                h5{
                    font-size: 30px;
                }
            }

            #month{
                background-color: #f3d0c7;
                width: 80px;
                text-align: center;
                padding-top: 5px;
            }
        }
    }
</style>