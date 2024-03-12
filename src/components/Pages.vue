<script>

export default {
    name: 'Pages',
}
</script>

<template>
    <div id="pages">
        <div id="title">
            <h1>
                Devotion that never <i>ends</i>
            </h1>
            <p>
                Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consecteur, adipisci velit, sed quia non numquam eius modi.
            </p>
            <button>
                Read more
            </button>
        </div>
        <div id="carousel">
           
        </div>
    </div>
</template>

<style lang="scss" scoped>
    #pages{
        max-width: 1500px;
        margin: 0 auto;
        height: 630px;
        display: flex;

        #title{
            padding: 100px;

            h1{
                font-size: 85px;
            }

            p{
                font-size: 22px;
            }
        }
    }
</style>