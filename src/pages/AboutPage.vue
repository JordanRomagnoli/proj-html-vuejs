<script>
export default {
    data() {
        return {

        }
    },
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
}
</style>
