<template>
  <article class="s5 relative" id="s5">
    <div class="top">
      <img src="./s5/bg.jpg" alt="bg">
      <img class="architecture" src="./s5/architecture.png" alt="architecture" data-aos="fade-up" data-aos-delay="3">
      <img class="title" src="./s5/title.svg" alt="title" data-aos="fade-right">
    </div>
    
    <div class="min">
      <img src="./s5/b_pic.jpg" alt="pic">
      <p class="font-['Noto_sans_tc'] text-[#000]">依政府公開計畫繪製，僅供參考，請依實際為主</p>
    </div>

    <div class="bottom">

    </div>
  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s5 {
  position: relative;
  overflow: hidden;

  .top {
    position: relative;
    .architecture {
      position: absolute;
      right: 0;
      bottom: 0;

      @media screen and (min-width: 768px) {
        width: size(1600);
      }
    }

    .title {
      position: absolute;

      @media screen and (min-width: 768px) {
        left: size(195);
        top: size(80);
      }
    }
  }

  .min {
    position: relative;
    img {
      width: 100%;
    }

    p {
      color: #000;
      font-weight: 400;
      line-height: 1.5;

      @media screen and (min-width: 768px) {
        font-size: size(15);
        right:size(10);
        bottom: size(10);
      }
    }
  }
  
}
</style>