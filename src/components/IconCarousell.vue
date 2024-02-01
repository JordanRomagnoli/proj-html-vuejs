<script>

import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';


import { Autoplay, } from 'swiper/modules';

export default {
    data() {
        return {
            iconsList: [
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
    methods: {
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
            
            modules: [Autoplay,],
        };
    },
}
</script>

<template>
    <div class="background">
        <div class=" container ">
            <swiper :slidesPerView="5" :spaceBetween="50" :loop="true" :modules="modules" class="mySwiper" :autoplay="{delay: 2500,disableOnInteraction: false,}">
                <swiper-slide v-for="(elem, i) in iconsList" :key="i">

                    <div class="icon-frame">
                        <img :src="getImagePath('../assets/img/' + elem.src)" alt="">
                    </div>
                </swiper-slide>
            </swiper>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/mixins' as *;


.background {
    @include background-cover('../assets/img/Parallax-03.jpg');

    .container {
        padding: 120px 0;
        position: relative;
    }
}



.icon-frame {
    width: 150px;
    height: 150px;

    img {
        @include img-frame;
        object-fit: contain;
    }
}
</style>
