<template>
  <article class="s6 relative" id="s6">
    <img class="bg" src="./s6/bg.webp" alt="bg">
    <h2 class="title" data-aos="zoom-in" data-aos-delay="0">自住宅 量身訂製</h2>
    

    <img class="pattern" src="./s6/pattern.svg" alt="pattern" data-aos="zoom-in" data-aos-delay="0">

    <img class="f" src="./s6/f.webp" alt="f" data-aos="fade-up" data-aos-delay="0">

    <img class="b_text" src="./s6/b_text.svg" alt="b_text" data-aos="zoom-in" data-aos-delay="0">

    <img class="b hidden md:block" src="./s6/b.webp" alt="b">
    <img class="b block md:hidden" src="./s6/b_m.png" alt="b">

      <p class="b_text2 font-['Noto_sans_tc'] text-[#fff]">
        智慧建築及綠建築標章依合法程序須待建築物取得使用執照後方可申請。預售時期僅提供候選證書。<br class="block md:hidden" />公司依銀級標章規格施工但是否取得銀級標章仍須主管機關審核同意｜外觀3D情境示意圖
      </p>
  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s6 {
  position: relative;
  height: sizem(630);

  @media screen and (min-width: 768px) {
    height: unset;
  }

  .bg {
    width: 100%;
    height: 100%;
    object-fit: cover;

    @media screen and (min-width: 768px) {
      height: unset;
      object-fit: unset;
    }
  }

  .b {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    margin: auto;
    z-index: 1;
    width: 100%;
  }

  .title {
    position: absolute;
    left: 0;
    right: 0;
    width: 100%;
      display: block;
        font-size:sizem(24);
        top: sizem(30);
        font-weight:600;
        text-align: center;
        color: #fff;
      @media screen and (min-width: 768px) {
        font-size:size(80);top: size(130);
      }
    }

  .pattern {
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    width: sizem(330);
    top: sizem(95);

    @media screen and (min-width: 768px) {
      width: size(915);
      top: size(300);
    }
  }

  .f {
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    width: sizem(130);
      bottom: sizem(65);

    @media screen and (min-width: 768px) {
      width: size(270);
      bottom: size(130);
    }
  }

  .b_text {
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    z-index: 2;
    width: sizem(300);
      bottom: sizem(45);
    @media screen and (min-width: 768px) {
      width: size(680);
      bottom: size(45);
    }
  }
  .b_text2 {
    position: absolute;
    left: .5em;
    right: .5em;
    margin: auto;
    z-index: 2;
      bottom: .5em;
      font-size:sizem(8);
      color: #fffc;
    @media screen and (min-width: 768px) {
    left: auto;
      font-size:size(15);
    }
  }
}
</style>