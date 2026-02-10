<template>
  <article class="s4 relative" id="s4">
    <div class="top_text">
      <h3 class="font-['Noto_sans_tc'] text-[#000]">
        全台唯一科技綠廊內的科學園區<br>
        後勁蛻變崛起，百公頃綠廊城市蓄勢而起
      </h3>
    </div>
    <div class="content">
      <img class="bg hidden md:block" src="./s4/bg.webp" alt="bg">
      <img class="bg block md:hidden" src="./s4/bg_m.jpg" alt="bg">

      <div class="text">
        <h2 class="title" data-aos="zoom-in" data-aos-delay="0">比鄰 兆元科技園區</h2>
        <p class="subtitle font-['Noto_sans_tc']" data-aos="zoom-in" data-aos-delay="0">2奈米先進製程 已於2025年底開始量產</p>
        <img class="pic" src="./s4/pic.svg" alt="pic" data-aos="zoom-in" data-aos-delay="0">
      </div>
      <p class="b_text font-['Noto_sans_tc'] text-[#fff]">
        職缺數量及完工時間點僅供參考 資料來源為自由新聞 正確的數據須依趨時為準<br class="block md:hidden" /> 高雄台積電實景拍攝 綠意合成示意圖
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

    padding-top: sizem(20);
    padding-bottom: sizem(20);

    @media screen and (min-width: 768px) {
      padding-top: size(35);
      padding-bottom: size(35);
    }

    h3 {
      font-weight: 400;
      line-height: 1.5;
      font-size: sizem(14);

      @media screen and (min-width: 768px) {
        font-size: size(35);
      }
    }
  }

  .content {
    position: relative;

    .bg {
      width: 100%;
    }

    .text {
      position: absolute;
      left: 0;
      right: 0;
      margin: auto;
      text-align: center;
      top: sizem(30);
      color: #fff;

      @media screen and (min-width: 768px) {
        top: size(90);
      }
      
    .title {
      display: block;
      margin-bottom: sizem(0);
        font-size:sizem(24);
        font-weight:600;

      @media screen and (min-width: 768px) {
        margin-bottom: size(10);
        font-size:size(80);
      }
    }

    .subtitle {
      font-size:sizem(14);
      font-weight:400;
      margin-bottom: sizem(10);
      @media screen and (min-width: 768px) {
        font-size:size(35);
      }
    }

      img {
        display: block;

        &.title {
          width: sizem(200);
          margin-bottom: sizem(10);

          @media screen and (min-width: 768px) {
            width: size(660);
          }
        }

        &.subtitle {
          width: sizem(245);
          margin-bottom: sizem(10);

          @media screen and (min-width: 768px) {
            margin-top: size(25);
            margin-bottom: size(25);
          }
        }

        &.pic {
          width: sizem(230);

          @media screen and (min-width: 768px) {
            width: size(650);
          }
        }
      }
    }

    .b_text {
      position: absolute;
      bottom: 0em;
      right: 0em;
      padding: .2em .5em;
      font-weight: 400;
      line-height: 1.3;
      font-size: sizem(10);
      text-align: right;
      text-shadow: 0 0 0.1em #000;

      @media screen and (min-width: 768px) {
        font-size: size(15);
      }
    }
  }
}
</style>