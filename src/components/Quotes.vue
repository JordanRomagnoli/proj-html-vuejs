<script>
import { Swiper, SwiperSlide } from 'swiper/vue';


import 'swiper/css';
import 'swiper/css/pagination';

import 'swiper/css/pagination';
import { Keyboard, Pagination, Navigation } from 'swiper/modules';

export default {
    data() {
        return {
            quotes: [
                {
                    quote: 'Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id.',
                    src: '01.jpg',
                    name: 'John Doe',
                    role: 'Designer',
                },
                {
                    quote: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
                    src: '02.jpg',
                    name: 'John Doe',
                    role: 'Designer',
                },
                {
                    quote: 'Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id.',
                    src: '03.jpg',
                    name: 'John Doe',
                    role: 'Designer',
                }
            ],

        };
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
            modules: [Keyboard, Pagination, Navigation],
        };
    },
};
</script>

<template>
    <div class="background">
        <div class="container">
            <div class="icon-frame">
                <img src="../assets/img/image(20).svg" alt="">
            </div>
            <swiper :slidesPerView="1" :spaceBetween="30" :keyboard="{
                enabled: true,
            }" :pagination="{
    clickable: true,
}" :navigation="true" :modules="modules" class="mySwiper">
                <swiper-slide v-for="(elem, i) in quotes">
                    <div class="quote-container">
                        <p>
                            {{ elem.quote }}
                        </p>
                        <div class="info-box">
                            <div class="image-frame">
                                <img :src="getImagePath('../assets/img/' + elem.src)" alt="">
                            </div>
                            <div class="profile">
                                <h4>
                                    {{ elem.name }}
                                </h4>
                                <span>{{ elem.role }}</span>
                            </div>
                        </div>
                    </div>
                </swiper-slide>

            </swiper>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.background {
    background-image: url(../assets/img/Parallax-02.jpg);
    background-attachment: fixed;
    padding: 60px 0;

    .container {
        overflow: hidden;
        position: relative;
        padding: 100px 0;

        .swiper {
            text-align: center;
            position: absolute;
            width: 100%;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: 0;
        }

        .icon-frame {
            margin: 0 auto;
            width: 100px;
            height: 100px;
            text-align: center;
            margin-bottom: 30px;

            img {
                width: 100%;
                height: 100%;
                object-fit: contain;
                z-index: 0;
                position: relative;
                bottom: 80px;
            }
        }

        .quote-container {
            color: white;
            text-align: center;
            margin-bottom: 60px;

            .quote {
                margin-bottom: 20px;
                text-align: center;
            }

            .info-box {
                display: flex;
                justify-content: center;

                .image-frame {
                    width: 50px;
                    height: 50px;
                    border-radius: 50%;
                    overflow: hidden;
                    margin-right: 10px;

                    img {
                        width: 100%;
                        height: 100%;
                        object-position: center;
                        object-fit: cover;
                    }
                }

                .profile {
                    text-align: start;
                }
            }
        }
    }
}
</style>
