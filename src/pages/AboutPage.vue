<script>
import { store } from '../store';
import Slider from '../components/Slider.vue';

export default {
    data() {
        return {
            store,
            listWatchedInAbout: [
                {
                    img: 'Gallery-01.jpg',
                    title: 'seventeenth summer',
                    subtitle: 'Commercial, Music Video'
                },
                {
                    img: 'Gallery-02.jpg',
                    title: 'a message to space',
                    subtitle: 'Short Film'
                },
                {
                    img: 'Gallery-03.jpg',
                    title: 'the most beautifull thing',
                    subtitle: 'Music Video'
                }
            ],
            teamUser: [
                {
                    img: '../assets/img/Team-01.jpg',
                    name: 'FABRICIO GUERRA',
                    role: 'Main Director'
                },
                {
                    img: '../assets/img/Team-02.jpg',
                    name: 'UMBERTO PAGODA',
                    role: 'Main Writer'
                },
                {
                    img: '../assets/img/Team-03.jpg',
                    name: 'GLORIA RICCASSO',
                    role: 'Main Producer'
                },
                {
                    img: '../assets/img/Team-04.jpg',
                    name: 'LIO NAPOIN',
                    role: 'Cameraman'
                }
            ]
        }
    },
    components: {
        Slider
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="container-about_page">

        <section class="jumbotron-about text-light">
            <h1 class="fw-bold mb-3">ABOUT</h1>

            <div class="return-home_page">
                <router-link class="text-light" :to="{ name: 'home' }">
                    Home
                </router-link>

                <span>/</span>

                <span>About</span>
            </div>
        </section>

        <section class="watchlist">
            <div class="text-center mb-3">
                <h6>
                    YOUR WATCHLIST
                </h6>

                <h2>
                    BEST HITS MOVIES
                </h2>
            </div>

            <div class="container d-flex">

                <div class="one-card p-3" v-for="(elem, i) in listWatchedInAbout">
                    <div class="card-img">
                        <img class="w-100" :src="getImagePath('../assets/img/' + (elem.img))">
                    </div>

                    <h5 class="text-center my-3 text-uppercase">
                        {{ elem.title }}
                    </h5>

                    <h6 class="text-body-secondary text-center">
                        {{ elem.subtitle }}
                    </h6>
                </div>

            </div>


        </section>

        <section class="about-us">
            <div class="container">

                <div>
                    <h6 class="text-uppercase fw-bold mb-4">
                        about us
                    </h6>

                    <h2 class="text-uppercase fw-bold mb-4">
                        high quality cinematics
                    </h2>

                    <p class="mb-5">
                        Orci varius penatibus et magnis dis parturient In the montes, nascetur ridiculus mus. Nulla
                        A nisi ut mi efficitur hendrerit. nunc urna. quisque a partr hendrerit purus erat, nec dapibus
                        sem sed. phasellus sed eli molestie, porttitor ligula of the egestas, mattis augue. quisque et
                        rhoncus justo. suspendisse luctus pharetra eleme tcondimentum.
                    </p>

                    <button type="button" class="text-uppercase py-3 px-5 fs-5 bg-light">
                        read more
                    </button>
                </div>

            </div>
        </section>

        <section class="meet-the-team">
            <div class="container">

                <div class="text-center">
                    <h6 class="text-uppercase mb-4">
                        the pericuros
                    </h6>

                    <h2 class="text-uppercase fw-bold mb-4">
                        meet the team
                    </h2>

                    <div class="d-flex">

                        <div class="user p-2" v-for="(elem, i) in teamUser">
                            <div class="img-user w-100">
                                <img class="w-100" :src="getImagePath(elem.img)" alt="">
                            </div>

                            <h5 class="fw-bold mt-4">
                                {{ elem.name }}
                            </h5>

                            <h6 class="text-body-secondary">
                                {{ elem.role }}
                            </h6>
                        </div>

                    </div>
                </div>

            </div>
        </section>

        <Slider />
    </div>
</template>

<style lang="scss" scoped>
.container-about_page {
    padding-top: 95px;

    .jumbotron-about {
        height: 280px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        background-image: url('../assets/img/bredcum-img.jpg');
        background-repeat: no-repeat;
        background-size: cover;


        h1 {
            font-size: 50px;
        }

        .return-home_page {
            font-size: 15px;
        }
    }

    .watchlist {
        padding: 80px 0;

        h2 {
            font-size: 2.8rem;
            font-weight: 700;
        }

        .one-card {
            width: calc(100% / 3);

            .card-img {
                overflow: hidden;

                img {
                    transition: all .3s ease-in-out;

                    &:hover {
                        transform: scale(1.1);
                    }
                }
            }
        }

    }

    .about-us {
        background-image: url('../assets/img/About-Us.jpg');
        background-repeat: no-repeat;
        background-size: cover;

        .container {
            padding-top: 100px;
            padding-bottom: 100px;
            color: white;

            div:first-of-type {
                width: 50%;
                margin-left: auto;

                p {
                    line-height: 35px;
                }

                button {
                    transition: color 0.5s;
                    color: white;

                    &:hover {
                        color: black;
                    }
                }
            }

        }
    }

    .meet-the-team {
        padding: 100px 0;

        .user {
            width: calc(100% / 4);

            .img-user {
                overflow: hidden;

                img {
                    transition: all .3s ease-in-out;

                    &:hover {
                        transform: scale(1.1);
                    }
                }
            }
        }
    }
}
</style>
