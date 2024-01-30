<script>
    export default {
        data() {
            return { 
                counterJumbotron: 0,
                jumbotronCarousellElement: [
                    {
                        img: 'blog01.jpg',
                        smallTitle: 'cinemato studio',
                        bigTitle:'action and inspire people',
                    },
                    {
                        img: 'blog02.jpg',
                        smallTitle: 'cinemato director',
                        bigTitle:'dancing with of the stars',
                    },
                ]
            }
        },
        methods:{

            nextButton(){
                if(this.counterJumbotron < this.jumbotronCarousellElement.length - 1){
                
                this.counterJumbotron ++;
        
                }else{
                    this.counterJumbotron = 0;
                }
            },

            prevButton(){
           
                if((this.counterJumbotron !== this.jumbotronCarousellElement.length) && (this.counterJumbotron !== 0)){

                    this.counterJumbotron -= 1 ;

                }else{
                    this.counterJumbotron = this.jumbotronCarousellElement.length - 1 ;
                }
            },
        }
    }
    </script>

<template>
    <div class="jumbotron" :class="{
        'active-1': counterJumbotron == 0,
        'active-2': counterJumbotron == 1,
    }">
       <div>
            
            <div class="container">
                <div class="row">
                    <div class="col-1">
                        <button @click="prevButton()">
                            <i class="fa-solid fa-chevron-left"></i>
                        </button>
                    </div>
                    <div class="col-10">
                        <h5>
                            {{ jumbotronCarousellElement[counterJumbotron].smallTitle }}
                        </h5>
                        <h1>
                            {{jumbotronCarousellElement[counterJumbotron].bigTitle}}
                        </h1>
                        <a href="#nogo">read more</a>
                    </div>
                    <div class="col-1">
                        <button @click="nextButton()">
                            <i class="fa-solid fa-chevron-right"></i>
                        </button>
                    </div>
                </div>
            </div>
       </div> 
    </div>
</template>

<style lang="scss" scoped>
    @use '../assets/scss/partials/variables' as *;

    .jumbotron{
        background-size: cover;
        background-position: center;
        transition: all .6s ease-in;

        > div{
            background-color: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 782px;
            padding: 20px;

                .container{
                    color: white;
                    .row{
                        padding: 0 20px;
                        .col-1{
                            display: flex;
                            align-items: center;
                            > button{
                                width: 50px;
                                height: 50px;
                                background-color: rgba(0, 0, 0, 0.5);
                                border: none;
                                color: white;
                            }
                        }
                        .col-10{
                            h1,h5,a{
                                text-transform: uppercase;
                            }
                            > h1{
                                font-size: 3.5rem;
                                font-weight: 700;
                                margin-bottom: 40px;
                            }
                            > a{
                                background-color: white;
                                color: black;
                                padding: 10px 40px;
                                font-size: 0.8rem;
                                border: none;
                                text-decoration: none;
                                font-weight: bold;
                            }
                        }
                        
                    }
                }
        }
    }

    .active-1{
        background-image: url(../assets/img/blog01.jpg);
    }
    .active-2{
        background-image: url(../assets/img/blog02.jpg);
    }
</style>
