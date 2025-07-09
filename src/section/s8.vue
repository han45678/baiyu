<template>
  <article class="s8 relative" id="s8">
    <div class="top">
      <h2 class="title" data-aos="zoom-in" data-aos-delay="0">興連城 用「心」連城</h2>
    
      <div class="banner">
        <img class="block md:hidden" src="./s8/pic_m.webp" alt="banner">
        <img class="hidden md:block" src="./s8/pic.webp" alt="banner">
      </div>
    </div>
    <div class="bottom">
      <h5 class="font-['Noto_sans_tc'] text-[#BB7430]">售後服務報修流程</h5>
      <div class="sop">
        <img src="./s8/1.svg" alt="order">
        <img src="./s8/2.svg" alt="order">
        <img src="./s8/3.svg" alt="order">
        <img src="./s8/4.svg" alt="order">
        <img src="./s8/5.svg" alt="order">
      </div>
      <h6 class="font-['Noto_serif_tc'] text-[#000]">
        盡心<span class="text-[#D27430]">｜</span>效率<span class="text-[#D27430]">｜</span>溫度
      </h6>
    </div>
  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s8 {
  .top {
    background-color: #fff;
    overflow: hidden;

    @media screen and (min-width: 768px) {
      padding-bottom: size(30);
    }

    .title {
      color: #004552;
      text-align: center;
      font-size:sizem(24);
      font-weight:600;
      margin-top: sizem(30);
      margin-bottom: sizem(10);
      @media screen and (min-width: 768px) {
        font-size:size(80);
        margin-top: size(85);
        margin-bottom: size(55);
      }
    }

    .banner {
      padding-bottom: sizem(15);

      @media screen and (min-width: 768px) {
        padding-bottom: 0;
      }

      img {
        width: 100%;
      }
    }
  }

  .bottom {
    h5 {
      text-align: center;
      font-weight: 400;
      line-height: 1.5;
      margin-top: sizem(15);
      margin-bottom: sizem(10);
      font-size: sizem(14);
      letter-spacing: sizem(1.96);

      @media screen and (min-width: 768px) {
        margin-top: size(25);
        margin-bottom: size(25);
        font-size: size(35);
        letter-spacing: size(4.9);
      }
    }

    .sop {
      width: 100%;
      margin-left: auto;
      margin-right: auto;
      display: flex;

      @media screen and (min-width: 768px) {
        max-width: size(1400);
        gap: size(30);
      }

      img {
        width: calc(100% / 5);
        background: linear-gradient(90deg, #fff0,#fffa, #FFF );

        @media screen and (min-width: 768px) {
          width: calc(100% / 5 - (size(30) / 5));
        }
      }
    }

    h6 {
      text-align: center;
      line-height: 1.35;
      font-weight: 600;
      margin-top: sizem(10);
      font-size: sizem(14);
      margin-bottom: sizem(20);
      @media screen and (min-width: 768px) {
        margin-top: size(25);
        font-size: size(35);
        margin-bottom: size(25);
      }
    }
  }
}
</style>