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
    <div class="singleCard">
        <div class="img-frame">
            <img :src="getImagePath('../assets/img/'+Image)" :alt="Title">
        </div>
        <h4>{{ Title }}</h4>
        <span>{{ Subtitle }}</span>
    </div>
</template>

<style lang="scss" scoped>
    @use '../assets/scss/partials/variables' as *;

    .singleCard{
        width: calc(100% / 4);
        padding: 0 15px;
        .img-frame{
            width: 100%;
            height: 400px;
            overflow: hidden;
            margin-bottom: 20px;
            img{
                width: 100%;
                height: 100%;
                object-fit: cover;
                object-position: center;
                transition: all .3s ease-in-out;
                &:hover{
                    transform: scale(1.05);
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
