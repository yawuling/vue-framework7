<template>
  <f7-page>
    <f7-navbar title="Swiper Slider" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        Framework7 comes with powerful and most modern touch slider ever - <a href="http://idangero.us/swiper/#.WXcyLmiGPIU" target="_blank">Swiper Slider</a> with super flexible configuration and lot, lot of features. Just check the following demos:
      </p>
    </f7-block>
    <f7-block-title>SWIPER EXAMPLES</f7-block-title>
    <f7-list>
      <f7-list-item v-for="(item, index) in items"
        :link="item.link"
        :title="item.title"
        :key="index"
      ></f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          title: 'Swiper Horizontal',
          link: '/swiperSlider/swiperHorizontal/'
        }, {
          title: 'Swiper Vertical',
          link: '/swiperSlider/swiperVertical/'
        }, {
          title: 'Space Between Slides',
          link: '/swiperSlider/spaceBetweenSwiper/'
        }, {
          title: 'Multiple Per Page',
          link: '/swiperSlider/multipleSlider/'
        }, {
          title: 'Nested Swipers',
          link: '/swiperSlider/nestedSliders/'
        }, {
          title: 'Infinite Loop Mode',
          link: '/swiperSlider/loopSlider/'
        }, {
          title: '3D Cube Effect',
          link: '/swiperSlider/3DCube/'
        }, {
          title: '3D Coverflow Effect',
          link: '/swiperSlider/3DCoverflow/'
        }, {
          title: '3D Flip Effect',
          link: '/swiperSlider/3DFlip/'
        }, {
          title: 'Fade Effect',
          link: '/swiperSlider/fadeEffect/'
        }, {
          title: 'With Scrollbar',
          link: '/swiperSlider/scrollbarSwiper/'
        }, {
          title: 'Two Way Control Gallery',
          link: '/swiperSlider/controlGallery/'
        }, {
          title: 'Custom Controls',
          link: '/swiperSlider/customSwiper/'
        }, {
          title: 'Parallax',
          link: '/swiperSlider/parallax/'
        }, {
          title: 'Lazy Loading',
          link: '/swiperSlider/sliderLazyloading/'
        }, {
          title: 'Progress Pagination',
          link: '/swiperSlider/progressPagination/'
        }, {
          title: 'Fraction Pagination',
          link: '/swiperSlider/fractionPagination/'
        }, {
          title: 'Zoom',
          link: '/swiperSlider/zoom/'
        }
      ]
    }
  }
}
</script>

<style lang="less">

</style>
