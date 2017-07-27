<template>
  <f7-page>
    <f7-navbar title="Color Themes" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        Framework7 comes with default 10 iOS color themes set and three layout color themes (default, dark and pure white):
      </p>
    </f7-block>
    <f7-block-title>CHOOSE LAYOUT THEME</f7-block-title>
    <f7-block>
      <f7-grid>
        <f7-col width="33" class="ks-layout-theme ks-layout-default">
          <div @click="changeLayout('layout-null')"></div>
        </f7-col>
        <f7-col width="33" class="ks-layout-theme ks-layout-dark">
          <div @click="changeLayout('layout-dark')"></div>
        </f7-col>
        <f7-col width="33" class="ks-layout-theme ks-layout-white">
          <div @click="changeLayout('layout-white')"></div>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block-title>CHOOSE COLOR THEME</f7-block-title>
    <f7-block>
      <f7-grid>
        <f7-col width="20" class="ks-color-theme bg-white">
          <div @click="changeColor('theme-white')"></div>
        </f7-col>
        <f7-col width="20" class="ks-color-theme bg-black">
          <div @click="changeColor('theme-black')"></div>
        </f7-col>
        <f7-col width="20" class="ks-color-theme bg-blue">
          <div @click="changeColor('theme-blue')"></div>
        </f7-col>
        <f7-col width="20" class="ks-color-theme bg-orange">
          <div @click="changeColor('theme-orange')"></div>
        </f7-col>
        <f7-col width="20" class="ks-color-theme bg-red">
          <div @click="changeColor('theme-red')"></div>
        </f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="20" class="ks-color-theme bg-pink">
          <div @click="changeColor('theme-pink')"></div>
        </f7-col>
        <f7-col width="20" class="ks-color-theme bg-green">
          <div @click="changeColor('theme-green')"></div>
        </f7-col>
        <f7-col width="20" class="ks-color-theme bg-lightblue">
           <div @click="changeColor('theme-lightblue')"></div>
        </f7-col>
        <f7-col width="20" class="ks-color-theme bg-yellow">
          <div @click="changeColor('theme-yellow')"></div>
        </f7-col>
        <f7-col width="20" class="ks-color-theme bg-gray">
          <div @click="changeColor('theme-gray')"></div>
        </f7-col>
      </f7-grid>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      themes: 'theme-white theme-black theme-yellow theme-red theme-blue theme-green theme-pink theme-lightblue theme-orange theme-gray',
      layouts: 'layout-dark layout-white'
    }
  },
  methods: {
    changeLayout: function (layout) {
      this.$$('body').removeClass(this.layouts).addClass(layout)
    },
    changeColor: function (color) {
      this.$$('body').removeClass(this.themes).addClass(color)
    }
  }
}
</script>

<style lang="less">
.ks-layout-theme{
  height: 44px;
  border: 1px solid rgba(0, 0, 0, 0.3);
  cursor: pointer;

  div{
    width: 100%;
    height: 100%;
  }
}
.ks-layout-default{
  background: #efeff4;
}
.ks-layout-dark{
  background: #222426;
}
.ks-layout-white{
  background: #fff;
}
.ks-color-theme{
  height: 44px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  cursor: pointer;
  margin-bottom: 10px;

  div{
    width: 100%;
    height: 100%;
  }
}
</style>
