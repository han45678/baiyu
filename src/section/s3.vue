<script setup>
import { ref } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation } from 'swiper'// 導入 Navigation 模組

import 'swiper/css'
import 'swiper/css/navigation'

// Swiper 設定
const swiperOptions = {
  modules: [Navigation], // 添加 Navigation 模組
  loop: true,
  navigation: {
    nextEl: '.custom-next',
    prevEl: '.custom-prev'
  },
  pagination: {
    clickable: false
  }
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

    <Swiper class="bg" :modules="[Navigation]" :navigation="{ nextEl: '.custom-next', prevEl: '.custom-prev' }" :loop="true">
      <SwiperSlide>
        <img src="./s3/bg1.jpg" alt="bg" />
        <img class="title" src="./s3/title.svg" alt="title">
      </SwiperSlide>
      <SwiperSlide>
        <img src="./s3/bg2.jpg" alt="bg" />
      </SwiperSlide>
      <SwiperSlide>
        <img src="./s3/bg3.jpg" alt="bg" />
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

    img {
      width: 100%;
      height: auto;
      display: block;

      &.title {
        position: absolute;
        left: 0;
        right: 0;
        margin: auto;
        z-index: 12;

        @media screen and (min-width: 768px) {
          top: size(120);
          width: size(820);;
        }
      }
    }
  }

  .nav-btn {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 37px;
    height: 66px;
    cursor: pointer;
    z-index: 10;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: opacity 0.3s;

    svg {
      width: 100%;
      height: auto;
    }

    &.custom-prev {
      left: 10px;
    }

    &.custom-next {
      right: 10px;
    }

    &:hover {
      opacity: 0.6;
    }
  }
}
</style>