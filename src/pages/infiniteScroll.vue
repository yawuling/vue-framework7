<template>
  <f7-page infinite-scroll @infinite="onInfiniteScroll">
    <f7-navbar title="Infinite Scroll" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>SCROLL BOTTOM</f7-block-title>
    <f7-list>
      <f7-list-item v-for="(item, index) in items" :title="'Item ' + item" :key="index"></f7-list-item>
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

      let self = this;

      setTimeout(function () {
        self.loading = false;

        if (self.items >= self.maxLength) {
          self.$f7.detachInfiniteScroll(self.$$('.infinite-scroll'))
          self.$$('.infinite-scroll-preloader').remove()
          return
        }

        self.items += 20;
      }, 1000)
    }
  }
}
</script>

<style lang="less">

</style>
