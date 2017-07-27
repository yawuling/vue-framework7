<template>
  <f7-page>
    <f7-navbar title="3D Flib" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-swiper :params="{ effect: 'flip' }" class="ks-flip-slider">
      <f7-swiper-slide v-for="(item, index) in items"
        :style="{ backgroundImage: 'url(' + item.img + ')'}"
        :key="index"
      >{{item.label}}</f7-swiper-slide>
    </f7-swiper>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          img: './static/image/slider1.jpg',
          label: 'Slide 1'
        }, {
          img: './static/image/slider2.jpg',
          label: 'Slide 2'
        }, {
          img: './static/image/slider3.jpg',
          label: 'Slide 3'
        }, {
          img: './static/image/slider4.jpg',
          label: 'Slide 4'
        }, {
          img: './static/image/slider5.jpg',
          label: 'Slide 5'
        }, {
          img: './static/image/slider6.jpg',
          label: 'Slide 6'
        }, {
          img: './static/image/slider7.jpg',
          label: 'Slide 7'
        }, {
          img: './static/image/slider8.jpg',
          label: 'Slide 8'
        }, {
          img: './static/image/slider9.jpg',
          label: 'Slide 9'
        }
      ]
    }
  }
}
</script>

<style lang="less" scoped>
.ks-flip-slider{
  width: 80%;
  height: 70%;
  top: 15%;
}
.swiper-slide{
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 25px;
  font-weight: 300;
  background-size: cover;
  color: #fff;
}
</style>
