<script>
export default {
    data() {
        return {
            headerItems: [
                'home',
                'blogs',
                'pages',
                'about',
                'contacts',
                'gallery',
                'shop'
            ],
            headerItems: [
                {
                    path: "/",
                    namePath: 'home'
                },
                {
                    path: "/blogs",
                    namePath: 'blogs'
                },
                {
                    path: "/pages",
                    namePath: 'pages'
                },
                {
                    path: "/about",
                    namePath: 'about'
                },
                {
                    path: "/contacts",
                    namePath: 'contacts'
                },
                {
                    path: "/gallery",
                    namePath: 'gallery'
                },
                {
                    path: "/shop",
                    namePath: 'shop'
                },
            ],
        }
    },
}
</script>

<template>
    <header>
        <div class="container-header d-flex justify-content-between align-items-center ">

            <div class="box-img">
                <router-link :to="{ name: 'home' }">
                    <img src="../assets/img/logo.svg" alt="">
                </router-link>
            </div>

            <div class="box-main-nav">
                <nav>
                    <ul class="list-unstyled d-flex align-items-center">
                        <li v-for="(elem, i) in headerItems" class="text-uppercase">

                            <router-link :to="elem.path">
                                {{ elem.namePath }}
                                <i class="fa-solid fa-angle-down" style="color: black;"></i>
                            </router-link>

                            <div class="dropdown-pages">
                                <div class="p-3">
                                    <a class="text-light" href="">
                                        services
                                    </a>
                                </div>
                                <div class="p-3 border-secondary border-top border-bottom">
                                    <a class="text-light" href="">
                                        our work flow
                                    </a>
                                </div>
                                <div class="p-3">
                                    <a class="text-light" href="">
                                        video thumbnail type
                                    </a>
                                </div>
                            </div>

                            <div class="dropdown-shop">

                                <div class="shop-links d-flex">

                                    <div class="d-flex justify-content-between align-items-center">
                                        <a class="text-light p-3" href="">
                                            shop pages
                                        </a>

                                        <i class="fa-solid fa-angle-right p-3" style="color: #c3c6d1;"></i>
                                    </div>

                                    <div class="dropright text-light">
                                        <div class="fw-bold p-3">
                                            my account
                                        </div>

                                        <div class="fw-bold p-3 border-secondary border-top border-bottom">
                                            checkout
                                        </div>

                                        <div class="fw-bold p-3">
                                            cart
                                        </div>
                                    </div>

                                </div>

                                <div class="shop-links d-flex border-top border-secondary">

                                    <div class="d-flex justify-content-between align-items-center">
                                        <a class="text-light p-3" href="">
                                            product type
                                        </a>

                                        <i class="fa-solid fa-angle-right p-3" style="color: #c3c6d1;"></i>
                                    </div>

                                    <div class="dropright text-light">
                                        <div class="fw-bold p-3">
                                            external/affiliate product
                                        </div>

                                        <div class="fw-bold p-3 border-top border-secondary">
                                            group product
                                        </div>

                                        <div class="fw-bold p-3 border-top border-secondary">
                                            simple product
                                        </div>

                                        <div class="fw-bold p-3 border-top border-secondary">
                                            variable product
                                        </div>
                                    </div>

                                </div>

                            </div>

                        </li>
                    </ul>
                </nav>
            </div>

            <div class="box-links d-flex justify-content-end">
                <div class="border-end border-dark">
                    <a href="">
                        <i class="fa-solid fa-magnifying-glass" style="color: black;"></i>
                    </a>
                </div>

                <div>
                    <a href="">
                        <i class="fa-brands fa-facebook-f" style="color: #000000;"></i>
                    </a>
                </div>

                <div>
                    <a href="">
                        <i class="fa-brands fa-twitter" style="color: #000000;"></i>
                    </a>
                </div>

                <div>
                    <a href="">
                        <i class="fa-brands fa-youtube" style="color: #000000;"></i>
                    </a>
                </div>

                <div>
                    <a href="">
                        <i class="fa-brands fa-instagram" style="color: #000000;"></i>
                    </a>
                </div>
            </div>

        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../assets/scss/header.scss' as *;
</style>
