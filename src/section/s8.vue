<template>
  <article class="s8 relative" id="s8">
    <div class="top">
      <div class="title">
        <img src="./s8/title.svg" alt="title">
      </div>
      <div class="banner">
        <img src="./s8/pic.png" alt="banner">
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

    @media screen and (min-width: 768px) {
      padding-bottom: size(30);
    }

    .title {
      text-align: center;

      img {
        @media screen and (min-width: 768px) {
          margin-top: size(85);
          margin-bottom: size(75);
        }
      }
    }

    .banner {
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
        @media screen and (min-width: 768px) {
        width: calc(100% / 5 - (size(30) / 5));
        }
      }
    }

    h6 {
      text-align: center;
      line-height: 1.35;
      font-weight: 600;

      @media screen and (min-width: 768px) {
        margin-top: size(25);
        font-size: size(35);
        margin-bottom: size(25);
      }
    }
  }
}
</style>