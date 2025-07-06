<template>
  <article class="s2 relative" id="s2">
    <img class="bg" src="./s2/bg.webp" alt="bg">
    <div class="text">
      <img class="title" src="./s2/title.svg" alt="title" data-aos="zoom-in" data-aos-delay="0">
      <img class="sub-title" src="./s2/subTitle.svg" alt="subTitle" data-aos="zoom-in" data-aos-delay="0">
    </div>
    <div class="building">
      <img src="./s2/building.webp" alt="building" data-aos="fade-up" data-aos-delay="3">
    </div>
    <div class="b_text font-['Noto_sans_tc'] text-[#fff]">半屏山 情境示意圖</div>
  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s2 {
  position: relative;
  .bg{
    width: 100%;
  }
  .text {
    position: absolute;
    z-index: 1;
    text-align: center;

    @media screen and (min-width: 768px) {
      top: size(120);
      left: 0;
      right: 0;
      margin: auto;

      .title {
        display: block;
        margin-bottom: size(37);
        width: size(660);
      }

      .sub-title {
        width: size(535);
      }
    }
  }

  .building {
    position: absolute;

    @media screen and (min-width: 768px) {
      left: size(290);
      bottom: 0;
    }

    img{
      @media screen and (min-width: 768px) {
        width: size(340);
      }
    }
  }

  .b_text {
    position: absolute;
    right: 0;
    bottom: 0;
    font-size: size(15);
    font-weight: 400;
    line-height: 150%;
    /* 22.5px */
  }
}
</style>