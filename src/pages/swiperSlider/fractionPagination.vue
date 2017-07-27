<template>
  <f7-page>
    <f7-navbar title="Slider Horizontal" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-swiper pagination :params="{ paginationType: 'fraction' }">
      <f7-swiper-slide v-for="(item, index) in items" :key="index">{{'Slide ' + item}}</f7-swiper-slide>
    </f7-swiper>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: 10
    }
  }
}
</script>

<style lang="less" scoped>
.swiper-container{
  height: 100%;
}
.swiper-slide{
  display: flex;
  justify-content: center;
  align-items: center;
  background:#fff;
  font-size: 25px;
}
</style>
