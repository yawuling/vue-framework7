<template>
  <f7-page>
    <f7-navbar title="Fade Effect" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-swiper pagination :params="{ effect: 'fade' }" class="ks-fade-slider">
      <f7-swiper-slide v-for="(item, index) in items"
        :style="{ backgroundImage: 'url(' + item + ')'}"
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
        './static/image/slider1.jpg',
        './static/image/slider2.jpg',
        './static/image/slider3.jpg',
        './static/image/slider4.jpg',
      ]
    }
  }
}
</script>

<style lang="less" scoped>
.ks-fade-slider{
  height: 100%;
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
</style>
