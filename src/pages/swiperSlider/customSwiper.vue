<template>
  <f7-page no-toolbar name="custom-swiper">
    <f7-navbar title="Custom Controls" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-swiper pagination next-button prev-button class="ks-custom-swiper">
      <f7-swiper-slide v-for="(item, index) in items"
        :style="{ backgroundImage: 'url(' + item + ')' }"
        :key="index"
      ></f7-swiper-slide>
    </f7-swiper>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: [
        './static/image/nightlife1.jpg',
        './static/image/nightlife2.jpg',
        './static/image/nightlife3.jpg',
        './static/image/nightlife4.jpg',
        './static/image/nightlife5.jpg',
        './static/image/nightlife6.jpg',
        './static/image/nightlife7.jpg'
      ]
    }
  }
}
</script>

<style lang="less">
.page[data-page="custom-swiper"]{
  .swiper-container{
    height: 100%;
  }
  .ks-custom-swiper{
    .swiper-slide{
      background-size: cover;
      background-position: center;
    }
    .swiper-pagination-bullet{
      cursor: pointer;
      width: 10px;
      height: 10px;
      background-color: rgba(255, 255, 255, 0);
      opacity: 1;
      border-radius: 0;
      transition: 200ms;
      box-sizing: border-box;
      border: 1px solid rgba(255, 255, 255, 0.8);
    }
    .swiper-pagination-bullet-active{
      border: 1px solid #007aff;
      transform: scale(1.4);
    }
  }
}
</style>
