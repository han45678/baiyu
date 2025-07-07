<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import SwiperCore, { Autoplay, FreeMode } from 'swiper'

SwiperCore.use([Autoplay])

import 'swiper/css'
</script>

<template>
  <article class="s5 relative" id="s5">
    <div class="top">
      <img class="bg" src="./s5/bg.webp" alt="bg">
      <img class="architecture" src="./s5/architecture.webp" alt="architecture" data-aos="fade-up" data-aos-delay="3">
      <img class="title" src="./s5/title.svg" alt="title" data-aos="fade-right">
    </div>

    <div class="min">
      <img src="./s5/b_pic.webp" alt="pic">
      <p class="font-['Noto_sans_tc'] text-[#000]">依政府公開計畫繪製，僅供參考，請依實際為主</p>
    </div>

    <div class="bottom">
      <div class="text">
        <img class="b_title" src="./s5/b_title.svg" alt="b_title" data-aos="zoom-in" data-aos-delay="0">
        <img class="mrt" src="./s5/mrt.svg" alt="mrt" data-aos="zoom-in" data-aos-delay="0">
      </div>
      <div class="stronghold">
        <img class="stronghold_img" src="./s5/stronghold.webp" alt="stronghold">
        <div class="train">
          <!-- 使用 Swiper 實現跑馬燈效果 -->
          <Swiper :modules="[Autoplay, FreeMode]" :loop="true" :slides-per-view="'auto'" :space-between="0"
            :freeMode="true" :freeModeMomentum="false" :allowTouchMove="false" :autoplay="{
              delay: 0,
              disableOnInteraction: false,
              pauseOnMouseEnter: false
            }" :speed="7000" class="marquee-swiper">
            <SwiperSlide v-for="n in 10" :key="n" style="width: auto;">
              <img src="./s5/train.webp" class="train-img" />
            </SwiperSlide>
          </Swiper>
        </div>
      </div>
    </div>
  </article>
</template>


<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s5 {
  position: relative;
  overflow: hidden;

  .top {
    position: relative;

    .bg {
      width: 100%;
    }

    .architecture {
      position: absolute;
      right: 0;
      bottom: 0;
      width: sizem(315);

      @media screen and (min-width: 768px) {
        width: size(1600);
      }
    }

    .title {
      position: absolute;
      left: sizem(25);
      top: sizem(15);
      width: sizem(185);

      @media screen and (min-width: 768px) {
        left: size(195);
        top: size(80);
        width: size(820);
      }

      .swiper-slide {
        width: auto !important;
      }


    }
  }

  .min {
    position: relative;

    img {
      width: 100%;
    }

    p {
      color: #000;
      font-weight: 400;
      line-height: sizem(20);
      font-size: sizem(10);
      background: #B9CCDA;
      text-align: right;
      padding-right: sizem(5);

      @media screen and (min-width: 768px) {
        position: absolute;
        font-size: size(15);
        right: size(10);
        bottom: size(10);
        background: transparent;
        padding-right: 0;
      }
    }
  }

  .bottom {
    .text {
      .b_title {
        display: block;
        margin-top: sizem(30);
        width: sizem(245);

        @media screen and (min-width: 768px) {
          margin-top: size(100);
          width: size(815);
        }
      }

      .mrt {
        display: block;
        margin-top: sizem(10);
        margin-bottom: sizem(50);
        width: sizem(360);

        @media screen and (min-width: 768px) {
          margin-top: size(20);
          margin-bottom: size(65);
          width: size(1000);
        }
      }
    }

    .stronghold {
      position: relative;
      pointer-events: none;

      .stronghold_img {
        width: 100%;
      }

      .train {
        position: absolute;
        left: 0;
        right: 0;
        margin: auto;
        bottom: 0;
        width: 100%;

        .train-img {
          width: auto;
          height: sizem(45);

          @media screen and (min-width: 768px) {
            height: size(100);
          }
        }
      }
    }
  }
}
</style>