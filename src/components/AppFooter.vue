<script>
export default {
    data() {
        return {
            datasInformation: [
                'Product Support',
                'Checkout',
                'Report Abuse',
                'Redeem Voucher',
                'Order Status'
            ],
            datasUsefulLinks: [
                'Policies & Rules',
                'Privacy Policy',
                'License Policy',
                'My account',
                'Locality'
            ]
        }
    },
}
</script>

<template>
    <footer>
        <div class="container">

            <div class="footer-top d-flex">
                <div class="col-footer py-3">
                    <h5 class="text-light">CONTACT INFO</h5>

                    <br>

                    <div class="mb-3">
                        <a class="d-flex" href="">
                            <div class="me-3">
                                <i class="fa-solid fa-location-dot fs-4" style="color: #c3c6d1;"></i>
                            </div>

                            <div class="fs-5">
                                2/45 Tower Street, New York USA
                            </div>
                        </a>
                    </div>

                    <div class="mb-3">
                        <a class="d-flex" href="">
                            <div class="me-3">
                                <i class="fa-solid fa-phone fs-4" style="color: #c3c6d1;"></i>
                            </div>

                            <div class="fs-5">
                                Call Us On 0800 840 1010
                            </div>
                        </a>
                    </div>

                    <div class="mb-3">
                        <a class="d-flex" href="">
                            <div class="me-3">
                                <i class="fa-solid fa-envelope fs-4" style="color: #c3c6d1;"></i>
                            </div>

                            <div class="fs-5">
                                Demo@Example.Com
                            </div>
                        </a>
                    </div>
                </div>

                <div class="col-footer py-3">
                    <h5 class="text-light">INFORMATION</h5>

                    <br>

                    <div class="fs-5 mb-2" v-for="(elem, i) in datasInformation">
                        <a class="fs-5" href="">{{ elem }}</a>
                    </div>
                </div>

                <div class="col-footer py-3">
                    <h5 class="text-light">USEFUL LINKS</h5>

                    <br>

                    <div class="fs-5 mb-2" v-for="(elem, i) in datasUsefulLinks">
                        <a class="fs-5" href="">
                            {{ elem }}
                        </a>
                    </div>
                </div>

                <div class="col-footer py-3">
                    <h5 class="text-light">NEWSLETTER</h5>

                    <br>

                    <div class="fs-5 mb-2">
                        Subscrive To Receive Inspiration, Ideas & News In Your Inbox.
                    </div>

                    <form>
                        <input class="bg-dark p-2 w-100 fs-5 border-0 mb-3" type="email" placeholder="Enter Your Email">

                        <button type="button" class="py-3 px-4 text-dark bg-light fs-6 fw-bold">
                            SUBSCRIBE
                        </button>
                    </form>
                </div>
            </div>

            <div class="footer-bottom border-top border-secondary color-light text-center py-4">
                © 2024 All Rights Reserved. Developed By TemplateMela
            </div>

        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../assets/scss/footer.scss' as *;
</style>
