<script>
export default {
    data() {
        return {
            interval: null,
            iconsSlider: [
                '../assets/img/01.png',
                '../assets/img/02.png',
                '../assets/img/03.png',
                '../assets/img/04.png',
                '../assets/img/05.png'
            ]
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="slider">
        <div class="container">

            <div class="box-slider">
                <div v-for="(elem, i) in iconsSlider">
                    <img :src="getImagePath(elem)" alt="">
                </div>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.slider {
    background-image: url('../assets/img/Parallax-03.jpg');
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    padding: 100px 0;

    .box-slider {
        display: flex;
        justify-content: space-around;

        >div {
            width: calc(100% / 5);
        }
    }
}
</style>
