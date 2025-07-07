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
  height: sizem(460);

  @media screen and (min-width: 768px) {
    height: unset;
  }

  .bg {
    width: 100%;
    height: 100%;
    object-fit: cover;

    @media screen and (min-width: 768px) {
      width: 100%;
    }
  }

  .text {
    position: absolute;
    z-index: 1;
    text-align: center;
    top: sizem(30);
    left: 0;
    right: 0;
    margin: auto;

    @media screen and (min-width: 768px) {
      top: size(120);
    }

    .title {
      display: block;
      width: sizem(200);
      margin-bottom: sizem(10);

      @media screen and (min-width: 768px) {
        margin-bottom: size(37);
        width: size(660);
      }
    }

    .sub-title {
      width: sizem(215);

      @media screen and (min-width: 768px) {
        width: size(535);
      }
    }
  }

  .building {
    position: absolute;
    left: sizem(35);
    bottom: 0;

    @media screen and (min-width: 768px) {
      left: size(290);
    }

    img {
      width: sizem(110);

      @media screen and (min-width: 768px) {
        width: size(340);
      }
    }
  }

  .b_text {
    position: absolute;
    right: sizem(10);
    bottom: sizem(5);
    font-size: sizem(10);
    font-weight: 400;
    line-height: 1.5;

    @media screen and (min-width: 768px) {
      font-size: size(15);
      right: 0;
      bottom: 0;
    }
  }
}
</style>