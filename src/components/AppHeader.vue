<script>
export default {
    data() {
        return {

        }
    },
}
</script>

<template>
    <header>
        <div class="container-header d-flex justify-content-between align-items-center ">

            <div class="box-img">
                <a href="">
                    <img src="../assets/img/logo.svg" alt="">
                </a>
            </div>

            <div class="box-main-nav">
                <nav>
                    <ul class="list-unstyled d-flex align-items-center">
                        <li>
                            <a href="">
                                home
                            </a>
                        </li>

                        <li>
                            <a href="">
                                Blogs
                            </a>
                        </li>

                        <li>
                            <a href="">
                                Pages
                                <i class="fa-solid fa-angle-down" style="color: black;"></i>
                            </a>
                        </li>

                        <li>
                            <a href="">
                                About
                            </a>
                        </li>

                        <li>
                            <a href="">
                                Contacts
                            </a>
                        </li>

                        <li>
                            <a href="">
                                Gallery
                            </a>
                        </li>

                        <li>
                            <a href="">
                                Shop
                                <i class="fa-solid fa-angle-down" style="color: black;"></i>
                            </a>
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
