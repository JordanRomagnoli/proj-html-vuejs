<script>
    export default {
        data() {
            return { 
                
            }
        },
        props: {
            Image: String,
            Title: String,
            Description: String,   
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
        <div class="icon-frame">
            <img :src="getImagePath('../assets/img/'+Image)" alt="">
        </div>
        <h3>
            {{ Title }}
        </h3>
        <p>
            {{ Description }}
        </p>
    </div>
</template>

<style lang="scss" scoped>
    @use '../assets/scss/partials/variables' as *;

    img{
        color: black;
    }

    .single-card{
        width: calc(100% / 3);
        padding: 10px;
        margin-bottom: 20px;
        .icon-frame{
            width: 80px;
            height: 80px;
            margin: 0 auto;
            margin-bottom: 40px;
            transition: all .2s ease-in-out;
            &:hover{
                transform: translateY(-10px);
            }

            img{
                width: 100%;
                height: 100%;
                object-fit: contain;
            }
        }
        > h3{
            text-transform: uppercase;
            font-size: 1.2rem;
        }
        > p{
            color: gray;
            line-height: 40px;
            font-size: 1.1rem;
        }
    }

</style>
