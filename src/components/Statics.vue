<script>
    export default {
        data() {
            return { 
                statics:[
                    {
                        number: 780,
                        trueNumber: 0,
                        title: 'satisfied client',
                    },
                    {
                        number: 20,
                        trueNumber: 0,
                        title: 'our project',
                    },
                    {
                        number: 10000,
                        trueNumber: 0,
                        title: 'cup of coffee',
                    },
                    {
                        number: 12,
                        trueNumber: 0,
                        title: 'our awards',
                    },
                    
                ]
            }
        },
        methods:{
            progressiveNumber(elem) {
                const intervalId = setInterval(() => {
                if (elem.trueNumber < elem.number) {
                elem.trueNumber++;
                } else {
                clearInterval(intervalId);
                }
            }, 1);
            },
        },
        created(){
            this.statics.forEach((elem) => {
            this.progressiveNumber(elem);
            });
        }
    }
    </script>

<template>
    <div class="background">
        <div class="container">
            <div class="row">
                <div class="col-3" v-for="(elem, i) in statics" :key="i">
                    <h4>
                        {{ elem.trueNumber }}
                    </h4>
                    <h5>
                        {{elem.title}}
                    </h5>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use '../assets/scss/partials/variables' as *;

    .background{
        background-image: url('../assets/img/Parallax-01.jpg');
        background-attachment: fixed;
        .row{
            min-height: 300px;
            align-items: center;
        }
    }

    .col-3{
        color: white;
        text-align: center;
        h4{
            font-size: 3rem;
            font-weight: bold;
        }
        h5{
            font-size: 1rem;
            font-weight: bolder;
            text-transform: uppercase;

        }
    }
</style>
