<template>
  <f7-page infinite-scroll @infinite="onInfiniteScroll">
    <f7-navbar title="Infinite Scroll" back-link="返回" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>SCROLL BOTTOM</f7-block-title>
    <f7-list>
      <f7-list-item v-for="item in items" :title="'Item ' + item"></f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: 20,
      loading: false,
      maxLength: 60
    }
  },
  methods: {
    onInfiniteScroll: function () {
      if (this.loading) {
        return;
      }

      this.loading = true;

      let _this = this;

      setTimeout(function () {
        _this.loading = false;

        if (_this.items >= _this.maxLength) {
          _this.$f7.detachInfiniteScroll(_this.$$('.infinite-scroll'))
          _this.$$('.infinite-scroll-preloader').remove()
          return
        }

        _this.items += 20;
      }, 1000)
    }
  }
}
</script>

<style lang="less">

</style>
