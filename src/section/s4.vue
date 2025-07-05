<template>
  <article class="s4 relative" id="s4">
    <div class="top_text">
      <h3 class="font-['Noto_sans_tc'] text-[#000]">
        全台唯一科技綠廊內的科學園區<br>
        後勁蛻變崛起，百公頃綠廊城市蓄勢而起
      </h3>
    </div>
    <div class="content">
      <img src="./s4/bg.png" alt="bg">
      <div class="text">
        <img class="title" src="./s4/title.svg" alt="title" data-aos="zoom-in" data-aos-delay="0">
        <img class="subtitle" src="./s4/subtitle.svg" alt="subtitle" data-aos="zoom-in" data-aos-delay="0">
        <img class="pic" src="./s4/pic.png" alt="pic" data-aos="zoom-in" data-aos-delay="0">
      </div>
      <p class="b_text font-['Noto_sans_tc'] text-[#fff]">
        高雄台積電實景拍攝 綠意合成示意圖
      </p>
    </div>
  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s4 {
  .top_text {
    text-align: center;
    background-color: #fff;

    @media screen and (min-width: 768px) {
      padding-top: size(35);
      padding-bottom: size(35);
    }

    h3 {
      font-weight: 400;
      line-height: 1.5;

      @media screen and (min-width: 768px) {
        font-size: size(35);
      }
    }
  }

  .content {
    position: relative;

    .text {
      position: absolute;
      left: 0;
      right: 0;
      margin: auto;
      text-align: center;

      @media screen and (min-width: 768px) {
        top: size(135);
      }

      img {
        display: block;

        &.subtitle {
          @media screen and (min-width: 768px) {
            margin-top: size(25);
            margin-bottom: size(25);
          }
        }
      }
    }

    .b_text {
      position: absolute;
      bottom: 0;
      right: 0;
      font-weight: 400;
      line-height: 1.5;

      @media screen and (min-width: 768px) {
        font-size: size(15);
      }
    }
  }
}
</style>