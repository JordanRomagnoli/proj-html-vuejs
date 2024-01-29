<script>
    export default {
        data() {
            return { 
                counterJumbotron: 0,
                jumbotronCarousellElement: [
                    {
                        img: '../assets/img/blog01.jpg',
                        smallTitle: 'cinemato studio',
                        bigTitle:'action and inspire people',
                    },
                    {
                        img: '../assets/img/blog02.jpg',
                        smallTitle: 'cinemato director',
                        bigTitle:'dancing with of the stars',
                    },
                ]
            }
        },
        methods:{
            
        }
    }
    </script>

<template>
    <div class="jumbotron">
        <button>
            prev
        </button>
        <div class="container">
            <div class="row">
                <div class="col-4">
                    <h4>
                        {{ jumbotronCarousellElement[0].smallTitle }}
                    </h4>
                    <h1>
                        {{jumbotronCarousellElement[0].bigTitle}}
                    </h1>
                    <button>read more</button>
                </div>
            </div>
        </div>
        <button>
            prev
        </button>
    </div>
</template>

<style lang="scss" scoped>
    @use '../assets/scss/partials/variables' as *;

    .jumbotron{
        min-height: 500px;
        padding: 20px;
        background-color: aqua;
        display: flex;
        align-items: center;
        background-size: cover;
        background-position: center;

        .container{
            border: 1px solid black;
            color: white;
            .row{
                h1,h4{
                    text-transform: uppercase;
                }
            }
        }
    }

    .active{
        background-image: url(../assets/img/blog01.jpg);
    }
</style>
