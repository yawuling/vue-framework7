<template>
  <f7-page name="parallax">
    <f7-navbar title="Slider Horizontal" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <div class="swiper-container swiper-init" data-pagination=".swiper-pagination" data-prev-button=".swiper-button-prev" data-next-button=".swiper-button-next" data-parallax="true" data-speed="600">
      <div class="parallax-bg" :style="{ backgroundImage: 'url(' + img + ')' }" data-swiper-parallax="-23%"></div>
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="(item, index) in items" :key="index">
          <div class="title" data-swiper-parallax="-100">{{item.title}}</div>
          <div class="subtitle" data-swiper-parallax="-200">{{item.subtitle}}</div>
          <div class="text" data-swiper-parallax="-300">
              <p>{{item.text}}</p>
          </div>
        </div>
      </div>
      <div class="swiper-button-prev swiper-button-white"></div>
      <div class="swiper-button-next swiper-button-white"></div>
      <div class="swiper-pagination swiper-pagination-white"></div>
    </div>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      img: './static/image/bnightlife2.jpg',
      items: [
        {
          title: 'Slide 1',
          subtitle: 'Subtitle',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam dictum mattis velit, sit amet faucibus felis iaculis nec. Nulla laoreet justo vitae porttitor porttitor. Suspendisse in sem justo. Integer laoreet magna nec elit suscipit, ac laoreet nibh euismod. Aliquam hendrerit lorem at elit facilisis rutrum. Ut at ullamcorper velit. Nulla ligula nisi, imperdiet ut lacinia nec, tincidunt ut libero. Aenean feugiat non eros quis feugiat.'
        }, {
          title: 'Slide 2',
          subtitle: 'Subtitle',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam dictum mattis velit, sit amet faucibus felis iaculis nec. Nulla laoreet justo vitae porttitor porttitor. Suspendisse in sem justo. Integer laoreet magna nec elit suscipit, ac laoreet nibh euismod. Aliquam hendrerit lorem at elit facilisis rutrum. Ut at ullamcorper velit. Nulla ligula nisi, imperdiet ut lacinia nec, tincidunt ut libero. Aenean feugiat non eros quis feugiat.'
        }, {
          title: 'Slide 3',
          subtitle: 'Subtitle',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam dictum mattis velit, sit amet faucibus felis iaculis nec. Nulla laoreet justo vitae porttitor porttitor. Suspendisse in sem justo. Integer laoreet magna nec elit suscipit, ac laoreet nibh euismod. Aliquam hendrerit lorem at elit facilisis rutrum. Ut at ullamcorper velit. Nulla ligula nisi, imperdiet ut lacinia nec, tincidunt ut libero. Aenean feugiat non eros quis feugiat.'
        }
      ]
    }
  }
}
</script>

<style lang="less">
.page[data-page="parallax"]{
  .swiper-container{
    height: 100%;
  }
  .swiper-slide{
    color: #fff;
    box-sizing: border-box;
    padding: 40px 60px;

    .title {
      font-size: 41px;
      font-weight: 300;
    }
    .subtitle {
      font-size: 21px;
    }
    .text {
      font-size: 14px;
      max-width: 400px;
      line-height: 1.3;
    }
  }
  .parallax-bg {
    position: absolute;
    left: 0;
    top: 0;
    width: 130%;
    height: 100%;
    background-size: cover;
    background-position: center;
  }
  .swiper-button-prev{
    background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D'http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg'%20viewBox%3D'0%200%2027%2044'%3E%3Cpath%20d%3D'M0%2C22L22%2C0l2.1%2C2.1L4.2%2C22l19.9%2C19.9L22%2C44L0%2C22L0%2C22L0%2C22z'%20fill%3D'%23ffffff'%2F%3E%3C%2Fsvg%3E");
  }
  .swiper-button-next{
    background-image: url("data:image/svg+xml;charset=utf-8,%3Csvg%20xmlns%3D'http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg'%20viewBox%3D'0%200%2027%2044'%3E%3Cpath%20d%3D'M27%2C22L27%2C22L5%2C44l-2.1-2.1L22.8%2C22L2.9%2C2.1L5%2C0L27%2C22L27%2C22z'%20fill%3D'%23ffffff'%2F%3E%3C%2Fsvg%3E");
  }
  .swiper-pagination-bullet-active{
    background-color: #fff;
  }
}
</style>
