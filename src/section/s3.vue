<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Autoplay } from 'swiper'// 導入 Navigation 模組

import 'swiper/css'
import 'swiper/css/navigation'

// Swiper 設定
const swiperOptions = {
  modules: [Navigation, Autoplay], // 添加 Navigation 模組
  loop: true,
  navigation: {
    nextEl: '.custom-next',
    prevEl: '.custom-prev'
  },
  pagination: {
    clickable: false
  },
  autoplay: {
    delay: 3500,
    disableOnInteraction: false
  },
  loop:true
}
</script>

<template>
  <article class="s3 relative" id="s3">
    <!-- 上一張 -->
    <div class="custom-prev nav-btn absolute left-2 top-1/2 -translate-y-1/2 z-10 cursor-pointer">
      <svg width="44" height="66" viewBox="0 0 44 66" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M41.7904 2.20959L11 33L41.7904 63.7904" stroke="white" stroke-width="5" />
        <path d="M34.7904 2.20959L4 33L34.7904 63.7904" stroke="black" stroke-width="5" />
      </svg>
    </div>

    <!-- 下一張 -->
    <div class="custom-next nav-btn absolute right-2 top-1/2 -translate-y-1/2 z-10 cursor-pointer">
      <svg width="44" height="66" viewBox="0 0 44 66" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M9.20959 63.7904L40 33L9.20959 2.20959" stroke="white" stroke-width="5" />
        <path d="M2.20959 63.7904L33 33L2.20959 2.20959" stroke="black" stroke-width="5" />
      </svg>
    </div>

    <Swiper class="bg" v-bind="swiperOptions">
      <SwiperSlide>
        <img src="./s3/bg1.webp" alt="bg" />
        <h2 class="title" data-aos="zoom-in" data-aos-delay="0">家前散策 生態綠廊公園</h2>
      </SwiperSlide>
      <SwiperSlide>
        <img src="./s3/bg2.webp" alt="bg" />
      </SwiperSlide>
      <SwiperSlide>
        <img src="./s3/bg3.webp" alt="bg" />
      </SwiperSlide>
    </Swiper>
  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s3 {
  position: relative;

  .bg {
    width: 100%;
    height: 100%;
    .title {
      position: absolute;
      text-align: center;
      color: #fff;
      font-size:sizem(24);
      font-weight:600;
      left: 0;
      right: 0;
      top: sizem(25);
      z-index: 12;
    
      @media screen and (min-width: 768px) {
        font-size:size(80);
          top: size(100);
         // width: size(820);
        }
    }
    img {
      width: 100%;
      height: auto;
      display: block;
    }
  }

  .nav-btn {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    cursor: pointer;
    z-index: 10;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: opacity 0.3s;
    height: sizem(6.75);
    width: sizem(13.5);

    @media screen and (min-width: 768px) {
      width: size(37);
      height: size(66);
    }

    svg {
      width: 100%;
      height: auto;
    }

    &.custom-prev {
      @media screen and (min-width: 768px) {
        left: size(10);
      }
    }

    &.custom-next {
      @media screen and (min-width: 768px) {
        right: size(10);
      }
    }

    &:hover {
      opacity: 0.6;
    }
  }
}
</style>