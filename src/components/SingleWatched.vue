<script>
    export default {
        data() {
            return { 
                
            }
        },
        props: {
            Image: String,
            Title: String,
            Subtitle: String,   
        },
        methods:{
            getImagePath: function(imgPath){
                return new URL(imgPath, import.meta.url).href;
            },
        }
    }
    </script>

<template>
    <div class="single-card">
        <div class="img-frame">
            <img :src="getImagePath('../assets/img/'+Image)" alt="">
        </div>
        <h4>
            {{ Title }}
        </h4>
        <span>
            {{ Subtitle }}
        </span>
    </div>    
</template>

<style lang="scss" scoped>
    @use '../assets/scss/partials/variables' as *;

    .single-card{
        width: calc(100% / 3);
        padding: 15px;
        text-align: center;
        margin-bottom: 20px;
        .img-frame{
            width: 100%;
            margin: 0 auto;
            overflow: hidden;
            margin-bottom: 20px;

            img{
                width: 100%;
                transition: all .4s ease-in-out;
                &:hover{
                    transform: scale(1.1);
                }
            }
        }
        > h4{
            text-transform: uppercase;
            font-size: 1.2rem;
            font-weight: 600;
        }
        > span{
            color: gray;
            font-size: 1.1rem;
        }
    }
</style>
