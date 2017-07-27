<template>
  <f7-page>
    <f7-navbar title="3D Coverflow Effect" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-swiper :params="{ effect: 'coverflow', slidesPerView: 'auto', centeredSlides: true }" class="ks-coverflow-slider">
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
          img: './static/image/bscenery1.jpg',
          label: 'Slide 1'
        }, {
          img: './static/image/bscenery2.jpg',
          label: 'Slide 2'
        }, {
          img: './static/image/bscenery3.jpg',
          label: 'Slide 3'
        }, {
          img: './static/image/bscenery4.jpg',
          label: 'Slide 4'
        }, {
          img: './static/image/bscenery5.jpg',
          label: 'Slide 5'
        }, {
          img: './static/image/bscenery6.jpg',
          label: 'Slide 6'
        }, {
          img: './static/image/bscenery7.jpg',
          label: 'Slide 7'
        }, {
          img: './static/image/bscenery8.jpg',
          label: 'Slide 8'
        }, {
          img: './static/image/bscenery9.jpg',
          label: 'Slide 9'
        }
      ]
    }
  }
}
</script>

<style lang="less" scoped>
.ks-coverflow-slider{
  height: 60%;
  top: 20%;
}
.swiper-slide{
  display: flex;
  width: 65%;
  justify-content: center;
  align-items: center;
  font-size: 25px;
  font-weight: 300;
  background-size: cover;
  color: #fff;
}
</style>
