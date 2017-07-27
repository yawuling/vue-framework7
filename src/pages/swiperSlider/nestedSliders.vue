<template>
  <f7-page>
    <f7-navbar title="Nested Sliders" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <div data-pagination=".swiper-pagination-h" class="swiper-container swiper-init">
      <div class="swiper-pagination swiper-pagination-h"></div>
      <div class="swiper-wrapper">
        <div class="swiper-slide"><span>Horizontal Slide 1</span></div>
        <div class="swiper-slide">
  
          <!-- Vertical nested child slider -->
          <div class="swiper-container swiper-init" data-pagination=".swiper-pagination-v" data-direction="vertical">
            <div class="swiper-pagination swiper-pagination-v"></div>
            <div class="swiper-wrapper">
              <div class="swiper-slide"><span>Vertical Slide 1</span></div>
              <div class="swiper-slide"><span>Vertical Slide 2</span></div>
              <div class="swiper-slide"><span>Vertical Slide 3</span></div>
            </div>
          </div>
  
        </div>
        <div class="swiper-slide"><span>Horizontal Slide 3</span></div>
        <div class="swiper-slide"><span>Horizontal Slide 4</span></div>
      </div>
    </div>
  </f7-page>
</template>

<script>
export default {

}
</script>

<style lang="less" scoped>
.swiper-container{
  height: 100%;
}
.swiper-container-vertical{
  width: 100%;
}
.swiper-slide{
  display: flex;
  justify-content: center;
  align-items: center;
  background:#fff;
  font-size: 25px;
}
</style>
