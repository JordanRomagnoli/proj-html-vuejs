<script>
    
    import { Swiper, SwiperSlide } from 'swiper/vue';
    import 'swiper/css';
    import 'swiper/css/pagination';
    

    import { Pagination } from 'swiper/modules';

    export default {
        data() {
            return { 
                iconsList:[
                    {
                        src: '',
                    },
                ]
            }
        },
        methods:{
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
            modules: [Pagination],
        };
        },
    }
</script>

<template>


</template>

<style lang="scss" scoped>
    @use '../assets/scss/partials/variables' as *;


</style>
