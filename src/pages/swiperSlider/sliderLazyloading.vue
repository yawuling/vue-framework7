<template>
  <f7-page>
    <f7-navbar title="Slider Lazy Loading" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-swiper pagination next-button prev-button :params="{ preloadImages: false, lazyLoading: true }" class="ks-lazy-slider">
      <f7-swiper-slide v-for="(item, index) in items" :key="index">
        <img :data-src="item" class="swiper-lazy" alt="" />
        <div class="preloader"></div>
      </f7-swiper-slide>
    </f7-swiper>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: [
        './static/image/xlscenery1.jpg',
        './static/image/xlscenery2.jpg',
        './static/image/xlscenery3.jpg',
        './static/image/xlscenery4.jpg',
        './static/image/xlscenery5.jpg',
        './static/image/xlscenery6.jpg',
        './static/image/xlscenery7.jpg',
        './static/image/xlscenery8.jpg',
        './static/image/xlscenery9.jpg',
        './static/image/xlscenery10.jpg'
      ]
    }
  }
}
</script>

<style lang="less">
.ks-lazy-slider{
  height: 100%;

  .swiper-slide{
    img{
      width: auto;
      height: auto;
      max-width: 100%;
      max-height: 100%;
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
    }
  }
  .preloader{
    width: 42px;
    height: 42px;
    position: absolute;
    left: 50%;
    top: 50%;
    margin-left: -21px;
    margin-top: -21px;
    z-index: 10;
  }
}
</style>
