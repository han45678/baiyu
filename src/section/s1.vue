<template>
  <article class="s1 relative" id="s1">
    <img class="bg_pc hidden md:block" src="./s1/bg.svg" alt="bg" />
    <img class="bg_pc block md:hidden" src="./s1/bgm.svg" alt="bg" />
    <div class="text">
      <div class="title" data-aos="zoom-in" data-aos-delay="0">
        <img class="title-bg hidden md:block" src="./s1/title_bg.svg" alt="title">
        <img class="title-bg block md:hidden" src="./s1/title_bg_m.svg" alt="title">
        <h2 class="title-main">生態綠廊<br class="block md:hidden"> 國家自然公園</h2>
      </div>
      <h3 class="sub-title  font-['Noto_Sans_TC']" data-aos="zoom-in" data-aos-delay="0">台積電園區 半導體兆元計畫</h3>
    </div>
    <img class="b_text" src="./s1/b_text.png" alt="b_text">
  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s1 {
  //height: sizem(604);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  position: relative;

  @media screen and (min-width: 768px) {
   // height: size(1350);
    justify-content: space-between;
    padding: 0;
  }

  .bg_pc {
    width: 100%;
   // min-height: 100%;
    background: url("./s1/bgm.jpg");
    background-size: cover;
    vertical-align: middle;

    @media screen and (min-width: 768px) {
      background-image: url("./s1/bg.jpg");
    }
  }

  .text {
    position: absolute;
    text-align: center;
    top: sizem(100);

    @media screen and (min-width: 768px) {
      top: size(125);
    }

    .title {
      position: relative;

      .title-bg {
        width: sizem(265);

        @media screen and (min-width: 768px) {
          width: size(995);
        }
      }

      .title-main {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: #c30c24;
        font-size:sizem(35);
        font-weight:600;
        line-height: 1.35;width: 100%;
        


        @media screen and (min-width: 768px) {
          font-size:size(80);
        }
      }
    }

    .sub-title {
      margin: sizem(20) auto 0 auto;
      font-size:sizem(17);

      @media screen and (min-width: 768px) {
        margin: size(45) auto 0 auto;
        font-size:size(35);
      }
    }
  }

  .b_text {
    font-size: sizem(12);
    position: absolute;
    bottom: 0;
    left: -1em;
    background: linear-gradient(185.5deg, #0000 50%, #000 100%);
    padding:1.75em 10em .5em 1.85em;
    height: 3.15em;
    @media screen and (min-width: 768px) {
      font-size: size(30);
      left: 0;
    }
  }
}
</style>