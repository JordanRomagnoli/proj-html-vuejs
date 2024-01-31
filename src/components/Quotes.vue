<script>
import Swiper from 'swiper';
import 'swiper/swiper-bundle.css';

export default {
  data() {
    return {
        counterSlide: 0,
        quotes: [
        {
          quote: 'Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id.',
          src: '01.jpg',
          name: 'John Doe',
          role: 'Designer',
        },
        {
          quote: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
          src: '02.jpg',
          name: 'John Doe',
          role: 'Designer',
        },
        {
          quote: 'Curabitur bibendum ex ut sapien blandit viverra. Nunc lobortis mi dui, id.',
          src: '03.jpg',
          name: 'John Doe',
          role: 'Designer',
        }
      ],
      
    };
  },
  methods: {
    getImagePath: function (imgPath) {
      return new URL(imgPath, import.meta.url).href;
    },

    firstButton(){
        this.counterSlide = 0;
    },

    secondButton(){
        this.counterSlide = 1;
    },

    thirdButton(){
        this.counterSlide = 2;
    },

  },
  created(){
  }
};
</script>

<template>
    <div class="background">
        <div class="container">
            <div class="icon-frame">
                <i class="fa-solid fa-quote-left"></i>
            </div>
            <div class="slide">
                <div class="quote">
                    <div>
                        {{ quotes[counterSlide].quote }}
                    </div>
                    <div>
                        {{ quotes[counterSlide].quote }}
                    </div>
                    <div>
                        {{ quotes[counterSlide].quote }}
                    </div>
                </div>
                
                <div class="info-box">
                    <div class="image-frame">
                        <img :src="getImagePath('../assets/img/'+quotes[counterSlide].src)" :alt="quotes[counterSlide].name">
                    </div>
                    <div>
                        <h4>
                            {{ quotes[counterSlide].name }}
                        </h4>
                        <span>{{ quotes[counterSlide].role }}</span>
                    </div>
                </div>
            </div>
            <div class="dot">
                <span @click="firstButton()">
                    <i class="fa-solid fa-circle"></i>
                </span>
                <span @click="secondButton()">
                    <i class="fa-solid fa-circle"></i>
                </span>
                <span @click="thirdButton()">
                    <i class="fa-solid fa-circle"></i>
                </span>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.background{
    background-image: url(../assets/img/Parallax-02.jpg);
    background-attachment: fixed;
    padding: 60px 0;
    .container{
    overflow: hidden;
    .icon-frame{
        margin: 0 auto;
        width: 10%;
        text-align: center;
        margin-bottom: 30px;
        i{
            font-size: 4rem;
            color: white;
        }
    }
    .slide{
        color: white;
        text-align: center;
        margin-bottom: 60px;
        .quote{
            margin-bottom: 20px;
            text-align: center;
        }
        .info-box{
            display: flex;
            justify-content: center;
            .image-frame{
                width: 50px;
                height: 50px;
                border-radius: 50%;
                overflow: hidden;
                margin-right: 10px;
                img{
                    width: 100%;
                    height: 100%;
                    object-position: center;
                    object-fit: cover;
                }
            }
        }
    }
    .dot{
        display: flex;
        justify-content: center;
        color: white;
        span{
            font-size: small;
            margin: 0 10px;
            cursor: pointer;
        }
    }
    }
}

</style>
