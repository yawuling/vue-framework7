<template>
  <f7-page>
    <f7-navbar title="Multiple Slider" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>1 SLIDE PER VIEW, 50PX BETWEEN</f7-block-title>
    <f7-swiper pagination :params="{ spaceBetween: 50 }">
      <f7-swiper-slide v-for="(item, index) in items" :key="index">{{'Slide ' + item}}</f7-swiper-slide>
    </f7-swiper>
    <f7-block-title>2 SLIDES PER VIEW, 20PX BETWEEN</f7-block-title>
    <f7-swiper pagination :params="{ spaceBetween: 20 }">
      <f7-swiper-slide v-for="(item, index) in items" :key="index">{{'Slide ' + item}}</f7-swiper-slide>
    </f7-swiper>
    <f7-block-title></f7-block-title>
    <f7-block-title>3 SLIDES PER VIEW, 10PX BETWEEN</f7-block-title>
    <f7-swiper pagination :params="{ spaceBetween: 10, slidesPerView: 3 }">
      <f7-swiper-slide v-for="(item, index) in items" :key="index">{{'Slide ' + item}}</f7-swiper-slide>
    </f7-swiper>
    <f7-block-title>AUTO SLIDES PER VIEW + CENTERED</f7-block-title>
    <f7-swiper pagination :params="{ spaceBetween: 10, slidesPerView: 'auto', centeredSlides: true }" class="ks-carousel-slider-auto">
      <f7-swiper-slide v-for="(item, index) in items" :key="index">{{'Slide ' + item}}</f7-swiper-slide>
    </f7-swiper>
    <f7-block-title>VERTICAL, 10PX BETWEEN</f7-block-title>
    <f7-swiper pagination :params="{ spaceBetween: 10, direction: 'vertical' }">
      <f7-swiper-slide v-for="(item, index) in items2" :key="index">{{'Slide ' + item}}</f7-swiper-slide>
    </f7-swiper>
    <f7-block-title>SLOW SPEED</f7-block-title>
    <f7-swiper pagination :params="{ spaceBetween: 50, speed: 900 }">
      <f7-swiper-slide v-for="(item, index) in items" :key="index">{{'Slide ' + item}}</f7-swiper-slide>
    </f7-swiper>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: 10,
      items2: 5
    }
  }
}
</script>

<style lang="less" scoped>
.swiper-container{
  height: 120px;
  font-size: 18px;
  margin: 0 0 35px;
}
.swiper-slide{
  display: flex;
  justify-content: center;
  align-items: center;
  box-sizing: border-box;
  border: 1px solid #ccc;
  background: #fff;
  font-weight: 300;
  font-size: 25px;
}
.ks-carousel-slider-auto{
  .swiper-slide{
    width: 85%;

    &:nth-child(2n){
      width: 70%;
    }
    &:nth-child(3n){
      width: 30%;
    }
  }
}
</style>
