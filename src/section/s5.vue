<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import SwiperCore, { Autoplay, FreeMode } from 'swiper'

SwiperCore.use([Autoplay])

import 'swiper/css'
</script>

<template>
  <article class="s5 relative" id="s5">
    <div class="top">
      <img class="architecture" src="./s5/architecture.webp" alt="architecture" data-aos="fade-up" data-aos-delay="3">
      <img class="title" src="./s5/title.svg" alt="title" data-aos="fade-right">
    </div>

    <div class="min">
      <img src="./s5/b_pic.webp" alt="pic">
      <p class="font-['Noto_sans_tc'] text-[#000]">依政府公開計畫繪製，僅供參考，請依實際為主</p>
    </div>

    <div class="bottom">
      <div class="text">
        <h2 class="title" data-aos="zoom-in" data-aos-delay="0"><span class="text-[#991F25]">R20</span>捷運 <span>500</span>米步行圈</h2>
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
    background:linear-gradient(0deg, rgba(147, 183, 220, 0.00) -39.82%, rgba(147, 183, 220, 0.04) -33.66%, rgba(147, 183, 220, 0.14) -24.42%, rgba(147, 183, 220, 0.30) -12.11%, rgba(147, 183, 220, 0.53) 1.75%, rgba(147, 183, 220, 0.83) 15.6%, #93B7DC 24.84%, #5880BE 84.88%, #416AB2 114.13%) ;
    height: sizem(133);
    @media screen and (min-width: 768px) {
      height: size(488);
    }
    .bg {
      width: 100%;
    }

    .architecture {
      position: absolute;
      right:sizem(-53);
      bottom: 0;
      //width: sizem(315);
      height:sizem(93);

      @media screen and (min-width: 768px) {
        right: 0;
        bottom: size(-90);
        height: size(395);
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
      line-height: 2;
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
    .title {
      display: block;
        font-size:sizem(24);
        margin-top: sizem(30);
        font-weight:600;
        text-align: center;
      @media screen and (min-width: 768px) {
        font-size:size(80);margin-top: size(100);
      }
      span{
        font-weight:400;font-size: 1.2em;
      }
    }

    .stronghold {
      position: relative;
      pointer-events: none;
      background: url("./s5/stronghold.svg") center center;
      background-size: sizem(470) auto;
      height:auto;
      @media screen and (min-width: 768px) {
      height:size(488);
      background-size: cover;
    }

      .stronghold_img {
      display: block;margin: auto;
      width: 100%;
      height:sizem(137);
      @media screen and (min-width: 768px) {
width: auto;
        height:100%;}
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