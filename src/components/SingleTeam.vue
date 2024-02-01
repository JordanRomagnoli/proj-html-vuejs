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
    @use '../assets/scss/partials/mixins' as *;

    .singleCard{
        width: calc(100% / 4);
        padding: 0 15px;
        .img-frame{
            width: 100%;
            height: 400px;
            overflow: hidden;
            margin-bottom: 20px;
            img{
                @include img-frame;
                object-fit: cover;
                @include img-transition;
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
