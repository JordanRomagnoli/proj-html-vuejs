<script>
    
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import 'swiper/css';
    import 'swiper/css/pagination';
    

    import { Pagination } from 'swiper/modules';

    export default {
        data() {
            return { 
                iconsList:[
                    {
                        src: '01.png',
                    },
                    {
                        src: '02.png',
                    },
                    {
                        src: '03.png',
                    },
                    {
                        src: '04.png',
                    },
                    {
                        src: '05.png',
                    },
                    {
                        src: '01.png',
                    },
                    {
                        src: '02.png',
                    },
                ]    
            }
        },
        methods:{
            getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
            },
        },
        components: {
            Swiper,
            SwiperSlide,
        },
        setup() {
        return {
            modules: [Pagination],
        };
        },
    }
</script>

<template>

<div class="background">
    <div class=" container ">
        <swiper
            :slidesPerView="5"
            :spaceBetween="50"
            :loop="true"
            
            :modules="modules"
            class="mySwiper"
        >
    <swiper-slide v-for="(elem, i) in iconsList"
    :key="i">

        <div class="icon-frame">
            <img :src="getImagePath('../assets/img/'+elem.src)" alt="">
        </div>
    </swiper-slide>
  </swiper>
    </div>
</div>

</template>

<style lang="scss" scoped>
    @use '../assets/scss/partials/variables' as *;

    .background{
        background-image: url(../assets/img/Parallax-03.jpg);
        background-size: cover;
        background-attachment: fixed;

        .container{

            padding: 60px 0;
        }
    }

    .swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}

.icon-frame{
    width: 150px;
    height: 150px;

    img{
        width: 100%;
        height: 100%;
        object-fit: contain;
        object-position: center;
    }
}
</style>
