<template>
  <f7-page>
    <f7-navbar title="Preloader" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        How about an activity indicator? Framework 7 has a nice one. The F7 preloader is made with SVG and animated with CSS so it can be easily resized. Two options are available: the default is for light background and another one is for dark background. The HTML is pretty easy, just add a .preloader class to any element. For the dark background option, also add a .preloader-white class. Here are some examples:
      </p>
    </f7-block>
    <f7-block style="text-align: center">
      <f7-grid>
        <f7-col width="25">
          <div>Default:</div>
          <f7-preloader></f7-preloader>
        </f7-col>
        <f7-col width="25" style="background-color: #222; color: #fff">
          <div>White:</div>
          <f7-preloader color="white"></f7-preloader>
        </f7-col>
        <f7-col width="25">
          <div>Big:</div>
          <f7-preloader size="42"></f7-preloader>
        </f7-col>        
        <f7-col width="25" style="background-color: #222; color: #fff">
          <div>White:</div>
          <f7-preloader color="white" size="42"></f7-preloader>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block>
      <p>
        Preloader also support all default color themes:
      </p>
      <f7-grid style="text-align: center">
        <f7-col width="25">
          <f7-preloader color="red"></f7-preloader>
        </f7-col>
        <f7-col width="25">
          <f7-preloader color="green"></f7-preloader>
        </f7-col>
        <f7-col width="25">
          <f7-preloader color="orange"></f7-preloader>
        </f7-col>
        <f7-col width="25">
          <f7-preloader color="blue"></f7-preloader>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block>
      <p>
        With app.showIndicator() you can call small overlay with indicator:
      </p>
      <f7-button @click="showIndicator">Open small indicator overlay</f7-button>
      <p>
        With app.showPreloader() you can call modal window with preloader:
      </p>
      <f7-button @click="showPreloader">Open preloader modal</f7-button>
      <p>With app.showPreloader('My text...') you can call it with custom title:</p>
      <f7-button @click="showCustomPreloader">Open custom preloader</f7-button>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  methods: {
    showIndicator: function () {
      let self = this

      self.$f7.showIndicator()
      setTimeout(function () {
        self.$f7.hideIndicator()
      }, 2000)
    },
    showPreloader: function () {
      let self = this

      self.$f7.showPreloader()
      setTimeout(function () {
        self.$f7.hidePreloader()
      }, 2000)
    },
    showCustomPreloader: function () {
      let self = this

      self.$f7.showPreloader('My text...')
      setTimeout(function () {
        self.$f7.hidePreloader()
      }, 2000)
    }
  }
}
</script>

<style lang="less">

</style>
