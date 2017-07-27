<template>
  <f7-page name="swiper-gallery">
    <f7-navbar title="Two Ways Control Garelly" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <div class="swiper-container ks-swiper-gallery-top">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="(item, index) in items"
          :style="{ backgroundImage: 'url(' + item + ')' }"
          :key="index"
        ></div>
      </div>
      <div class="swiper-button-next"></div>
      <div class="swiper-button-prev"></div>
    </div>
    <div class="swiper-container ks-swiper-gallery-thumbs">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="(item, index) in items"
          :style="{ backgroundImage: 'url(' + item + ')' }"
          :key="index"
        ></div>
      </div>
    </div>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: [
        './static/image/bscenery1.jpg',
        './static/image/bscenery2.jpg',
        './static/image/bscenery3.jpg',
        './static/image/bscenery4.jpg',
        './static/image/bscenery5.jpg',
        './static/image/bscenery6.jpg',
        './static/image/bscenery7.jpg',
        './static/image/bscenery8.jpg',
        './static/image/bscenery9.jpg'
      ]
    }
  },
  mounted () {
    //control类型为“Swiper Instance”，因此只能用js初始化

    let swiperTop = this.$f7.swiper('.ks-swiper-gallery-top', {
      nextButton: '.swiper-button-next',
      prevButton: '.swiper-button-prev',
      spaceBetween: 10
    })
    let swiperThumbs = this.$f7.swiper('.ks-swiper-gallery-thumbs', {
      slidesPerView: 'auto',
      spaceBetween: 10,
      centeredSlides: true,
      touchRatio: 0.2,
      slideToClickedSlide: true
    })
    swiperTop.params.control = swiperThumbs
    swiperThumbs.params.control = swiperTop
  }
}
</script>

<style lang="less">
.page[data-page="swiper-gallery"]{
  background-color: #000;

  .ks-swiper-gallery-top{
    height: 70%;
  }
  .ks-swiper-gallery-thumbs{
    margin-top: 10px;
    height: 20%;
    height: calc(~"30% - 20px");

    .swiper-slide{
      width: 25%;
    }
  }
  .swiper-slide{
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 25px;
    font-weight: 300;
    background-size: cover;
    background-position: center;
    color: #fff;
  }
  .swiper-button-prev{
    background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D'http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg'%20viewBox%3D'0%200%2027%2044'%3E%3Cpath%20d%3D'M0%2C22L22%2C0l2.1%2C2.1L4.2%2C22l19.9%2C19.9L22%2C44L0%2C22L0%2C22L0%2C22z'%20fill%3D'%23ffffff'%2F%3E%3C%2Fsvg%3E");
  }
  .swiper-button-next{
    background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D'http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg'%20viewBox%3D'0%200%2027%2044'%3E%3Cpath%20d%3D'M27%2C22L27%2C22L5%2C44l-2.1-2.1L22.8%2C22L2.9%2C2.1L5%2C0L27%2C22L27%2C22z'%20fill%3D'%23ffffff'%2F%3E%3C%2Fsvg%3E");
  }
}
</style>
