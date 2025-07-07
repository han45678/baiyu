<template>
  <article class="s6 relative" id="s6">
    <img class="bg" src="./s6/bg.webp" alt="bg">

    <img class="title" src="./s6/title.svg" alt="title" data-aos="zoom-in" data-aos-delay="0">

    <img class="pattern" src="./s6/pattern.svg" alt="pattern" data-aos="zoom-in" data-aos-delay="0">

    <img class="f" src="./s6/f.webp" alt="f" data-aos="fade-up" data-aos-delay="0">

    <img class="b_text" src="./s6/b_text.svg" alt="b_text" data-aos="zoom-in" data-aos-delay="0">

    <img class="b hidden md:block" src="./s6/b.webp" alt="b">
    <img class="b block md:hidden" src="./s6/b_m.webp" alt="b">

  </article>
</template>

<style lang="scss" scoped>
@import '@/assets/style/function.scss';

.s6 {
  position: relative;
  height: sizem(600);

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
    margin: auto;
    width: sizem(175);
    top: sizem(30);

    @media screen and (min-width: 768px) {
      width: size(580);
      top: size(130);
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
      bottom: sizem(55);

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
    width: sizem(260);
      bottom: sizem(25);
    @media screen and (min-width: 768px) {
      width: size(655);
      bottom: size(45);
    }
  }
}
</style>