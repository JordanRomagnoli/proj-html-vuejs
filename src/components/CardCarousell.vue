<script>

import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation } from 'swiper/modules';

export default {
    data() {
        return {
            cardList1: [
                {
                    image: 'blog01.jpg',
                    date: 'November 06, 2021 By Admin',
                    title: 'recap your latestcompany event',
                    description: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed',
                },
                {
                    image: 'blog02.jpg',
                    date: 'May 27, 2022 By Admin',
                    title: 'how to edit a film score to serve',
                    description: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed',
                },
                {
                    image: 'blog03.jpg',
                    date: 'May 07, 2022 By Admin',
                    title: 'are you ready to make it awesome',
                    description: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed',
                },
            ],
            cardList2: [
                {
                    image: 'blog04.jpg',
                    date: 'April 10, 2022 By Admin',
                    title: 'last video website you need for',
                    description: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed',
                },
                {
                    image: 'blog05.jpg',
                    date: 'Marc 01, 2022 By Admin',
                    title: 'band uprising to cult status',
                    description: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed',
                },
                {
                    image: 'blog06.jpg',
                    date: 'February 14, 2022 By Admin',
                    title: 'bringing the stage to life',
                    description: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed',
                },
            ],
            cardList3: [
                {
                    image: 'blog07.jpg',
                    date: 'December 07, 2021 By Admin',
                    title: 'cadenze rios picked for the next picture',
                    description: 'Suspendisse dictum dictum tempor. Ut non faucibus arcu, id elementum est. Suspendisse sed',
                },
            ],
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
            modules: [Navigation],
        };
    },
}
</script>

<template>
    <div class="container">
        <h6>
            latest news
        </h6>
        <h2>
            articles updated daily
        </h2>
        <div class="container-swiper">
            <swiper :navigation="true" :modules="modules" class="mySwiper">
                <swiper-slide class="row g-0 ">
                    <div class="single-card" v-for="(elem, i) in cardList1">
                        <div class="img-frame">
                            <img :src="getImagePath('../assets/img/' + elem.image)" alt="">
                        </div>
                        <span>{{ elem.date }}</span>
                        <h3>{{ elem.title }}</h3>
                        <p>{{ elem.description }}</p>
                    </div>
                </swiper-slide>

                <swiper-slide class="row g-0 ">
                    <div class="single-card" v-for="(elem, i) in cardList2">
                        <div class="img-frame">
                            <img :src="getImagePath('../assets/img/' + elem.image)" alt="">
                        </div>
                        <span>{{ elem.date }}</span>
                        <h3>{{ elem.title }}</h3>
                        <p>{{ elem.description }}</p>
                    </div>
                </swiper-slide>

                <swiper-slide class="row g-0 ">
                    <div class="single-card" v-for="(elem, i) in cardList3">
                        <div class="img-frame">
                            <img :src="getImagePath('../assets/img/' + elem.image)" alt="">
                        </div>
                        <span>{{ elem.date }}</span>
                        <h3>{{ elem.title }}</h3>
                        <p>{{ elem.description }}</p>
                    </div>
                </swiper-slide>
            </swiper>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.container {
    padding: 60px 0;
    text-align: center;

    .container-swiper {
        padding-bottom: 40%;
        width: 100%;
        position: relative;

        .mySwiper {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            z-index: 0;
        }
    }
}

.swiper {
    width: 100%;
    height: 100%;

    .swiper-slide {
        text-align: center;
        font-size: 18px;
        display: flex;
        justify-content: flex-start;
        align-items: center;


        .single-card {
            width: calc(100% / 3);
            padding: 0 10px;

            .img-frame {
                cursor: pointer;
                width: 100%;
                height: 300px;
                margin-bottom: 20px;
                overflow: hidden;

                img {
                    width: 100%;
                    height: 100%;
                    object-fit: cover;
                    object-position: center;
                    transition: all .3s ease-in-out;

                    &:hover {
                        transform: scale(1.1);
                    }
                }
            }

            span {
                font-size: 0.9rem;
                color: gray;
                font-weight: bolder;

            }

            h3 {
                text-transform: uppercase;
                font-size: 1.1rem;
                font-weight: bolder;
                margin: 20px 0;
            }

            p {
                font-size: 0.9rem;
                line-height: 25px;
            }
        }
    }
}

.swiper-button-prev,
.swiper-button-next {
    display: none;

    &:hover {
        display: block;
    }
}


h6,
h2 {
    text-transform: uppercase;
}

h2 {
    font-size: 2.8rem;
    font-weight: 700;
    margin-bottom: 20px;
}
</style>
