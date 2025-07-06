<script setup>
import { ref } from "vue"

const splide = ref(null);

const sConfig = {
  autoWidth: true,
  arrows: false,
  autoplay: true,
  pagination: false,
  drag: true,
  interval: 5000, // 調整跑馬燈速度，speed/interval須一致
  speed: 5000, // 調整跑馬燈速度，speed/interval須一致
  snap: false,
  easing: "linear",
  gap: 0,
  loop:true,
  type: "loop",
  perMove: 1,
}

</script>

<template>
  <article class="s7 relative" id="s7">
    <div class="logo">
      <img class="bg" src="./s7/logo_bg.webp" alt="bg">
      <img class="logoPic" src="./s7/logo.svg" alt="logo">
    </div>
    <div class="content">
      <img class="bg" src="./s7/bg.webp" alt="bg">
      <div class="content_wrapper">
        <div class="manager">
          <img src="./s7/manager.webp" alt="manager" data-aos="fade-right" data-aos-delay="0">
        </div>
        <div class="text">
          <img class="title" src="./s7/title.svg" alt="title" data-aos="fade-right" data-aos-delay="0">
          <img class="en_text" src="./s7/text.svg" alt="text" data-aos="fade-right" data-aos-delay="0">
        </div>
      </div>
    </div>
    <div class="bottom">
      <img class="bg" src="./s7/b_bg.webp" alt="bg">
      <Splide :options="sConfig" ref="splide" class="slide">
        <SplideSlide class="slide-item">
          <img src="./s7/1.svg" alt="pic">
        </SplideSlide>
        <SplideSlide class="slide-item">
          <img src="./s7/2.svg" alt="pic">
        </SplideSlide>
        <SplideSlide class="slide-item">
          <img src="./s7/3.svg" alt="pic">
        </SplideSlide>
        <SplideSlide class="slide-item">
          <img src="./s7/4.svg" alt="pic">
        </SplideSlide>
        <SplideSlide class="slide-item">
          <img src="./s7/5.svg" alt="pic">
        </SplideSlide>
        <SplideSlide class="slide-item">
          <img src="./s7/6.svg" alt="pic">
        </SplideSlide>
        <SplideSlide class="slide-item">
          <img src="./s7/7.svg" alt="pic">
        </SplideSlide>
        <SplideSlide class="slide-item">
          <img src="./s7/8.svg" alt="pic">
        </SplideSlide>
        <SplideSlide class="slide-item">
          <img src="./s7/9.svg" alt="pic">
        </SplideSlide>
      </Splide>
    </div>
  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s7 {
  .logo {
    position: relative;

    .bg{
      width: 100%;
    }
    .logoPic {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
    }
  }

  .content {
    position: relative;
    .bg{
      width: 100%;
    }
    .content_wrapper {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      top: 0;
      margin: auto;
      display: flex;
      align-items: flex-end;

      .manager {
        width: 45%;

        img {
          width: 100%;
        }
      }

      .text {
        width: 55%;

        .title {
          @media screen and (min-width: 768px) {
            margin-top: size(100);
            width: size(580);
          }
        }

        .en_text {
          @media screen and (min-width: 768px) {
            width: size(965);
            margin-top: size(150);
          }
        }
      }
    }
  }

  .bottom {
    position: relative;
.bg{
      width: 100%;
    }
    .slide {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      margin: auto;

      .slide-item {
        @media screen and (min-width: 768px) {
          width: size(220);
          margin-right: size(39);
        }
        img{
          width: 100%;
        }
      }
    }
  }
}
</style>