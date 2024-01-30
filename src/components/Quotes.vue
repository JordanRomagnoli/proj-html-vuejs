<script>
import Swiper from 'swiper';
import 'swiper/swiper-bundle.css';

export default {
  data() {
    return {
      firstQuote: [
        {
          quote: 'Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id. Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id.',
          src: '01.jpg',
          name: 'John Doe',
          role: 'Designer',
        }
      ],

      secondQuote: [
        {
          quote: 'Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id. Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id.',
          src: '02.jpg',
          name: 'John Doe',
          role: 'Designer',
        }
      ],

      thirdQuote: [
        {
          quote: 'Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id. Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id.',
          src: '03.jpg',
          name: 'John Doe',
          role: 'Designer',
        }
      ],
      swiper: null,
    };
  },
  methods: {
    getImagePath: function (imgPath) {
      return new URL(imgPath, import.meta.url).href;
    },

    initSwiper() {
      this.swiper = new Swiper('.swiper-container', {
        loop: true,
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
      });
    },
  },
  mounted() {
    this.initSwiper();
  },
};
</script>

<template>
    <div class="background">
        <div class="container">
                <div>
                    <i class="fa-solid fa-quote-right"></i>
                </div>
            <div class="frame">
                <div class="swiper-container">
                <div class="swiper-wrapper">
                <div class="swiper-slide">
                    <div>
                    {{ firstQuote[0].quote }}
                    </div>
                    <div class="info">
                        <div class="icon-frame">
                            <img :src="getImagePath('assets/img/' + firstQuote[0].src)" alt="">
                        </div>
                        <div>
                        <h4>{{ thirdQuote[0].name }}</h4>
                        <span>{{ thirdQuote[0].role }}</span>
                    </div>
                    </div>
                </div>

                <div class="swiper-slide">
                    <div>
                    {{ secondQuote[0].quote }}
                    </div>
                    <div class="info">
                        <div class="icon-frame">
                            <img :src="getImagePath('assets/img/'+secondQuote[0].src)" alt="">
                        </div>
                        <div>
                        <h4>{{ thirdQuote[0].name }}</h4>
                        <span>{{ thirdQuote[0].role }}</span>
                    </div>
                    </div>
                </div>

                <div class="swiper-slide">
                    <div>
                    {{ thirdQuote[0].quote }}
                    </div>
                    <div class="info">
                        <div class="icon-frame">
                            <img :src="getImagePath('assets/img/' + thirdQuote[0].src)" alt="">
                        </div>
                        <div>
                        <h4>{{ thirdQuote[0].name }}</h4>
                        <span>{{ thirdQuote[0].role }}</span>
                    </div>
                    </div>
                </div>
            </div>
        <div class="swiper-button-next"></div>
        <div class="swiper-button-prev"></div>
                </div>

            </div>
            
        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.background{
    background-image: url(../assets/img/Parallax-02.jpg);
    background-attachment: fixed;
}
.container{
    overflow: hidden;
    .frame{
        height: 400px;
        display: flex;
        align-items: center;
    }
}

.icon-frame{
    width: 80px;
    height: 80px;
    img{
        width: 100%;
        height: 100%;
    }
}
.info{
    display: flex;
    justify-content: center;
}
.swiper-container {
  width: 100%;
  .swiper-slide{
    text-align: center;
    color: white;
  }
}
</style>
