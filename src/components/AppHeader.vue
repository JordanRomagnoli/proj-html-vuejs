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

                    <button class="search-button border-0 pe-3" type="button" data-bs-toggle="offcanvas"
                        data-bs-target="#offcanvasExample" aria-controls="offcanvasExample">
                        <i class="fa-solid fa-magnifying-glass fs-4" style="color: #000000;"></i>
                    </button>

                    <div class="offcanvas  offcanvas-start w-100" tabindex="-1" id="offcanvasExample"
                        aria-labelledby="offcanvasExampleLabel">

                        <div class="offcanvas-header">
                            <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas"
                                aria-label="Chiudi">
                                <i class="fa-solid fa-xmark fs-3" style="color: #ffffff;"></i>
                            </button>
                        </div>

                        <div class="offcanvas-body d-flex justify-content-center align-items-center">

                            <form class="d-flex border border-light p-4 w-50">
                                <input class="form-control bg-special border-0 text-light rounded-0" type="search"
                                    placeholder="search" aria-label="Search">
                                <button class="bg-special border-0" type="submit">
                                    <i class="fa-solid fa-magnifying-glass fs-4" style="color: white;"></i>
                                </button>
                            </form>

                        </div>

                    </div>

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
