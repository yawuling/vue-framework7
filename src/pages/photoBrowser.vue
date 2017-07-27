<template>
  <f7-page>
    <f7-navbar title="Photo Browser" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        Photo Browser is a standalone and highly configurable component that allows to open window with photo viewer and navigation elements with the following features:
      </p>
      <ul>
        <li>Swiper between photos</li>
        <li>Multi-gestures support for zooming</li>
        <li>Toggle zoom by double tap on photo</li>
        <li>Single click on photo to toggle Exposition mode</li>
      </ul>
      <p>
        Photo Browser could be opened in a three ways - as a Standalone component, in Popup, and as separate Page:
      </p>
      <f7-grid>
        <f7-col width="33">
          <f7-button @click="onStandalone">Standalone</f7-button>
        </f7-col>
        <f7-col width="33">
          <f7-button @click="onPopup">Popup</f7-button>
        </f7-col>
        <f7-col width="33">
          <f7-button @click="onPage">Page</f7-button>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block>
      <p>
        For Popup and Standalone types, Photo Browser suppots 2 default themes - default Light (like in previous examples) and Dark theme. Here is a Dark theme examples:
      </p>
      <f7-grid>
        <f7-col width="50">
          <f7-button @click="onDarkStandalone">Standalone</f7-button>
        </f7-col>
        <f7-col width="50">
          <f7-button @click="onDarkPopup">Popup</f7-button>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block>
      <p>
        Photo Browser also supports lazy loading for passed images:
      </p>
      <p>
        <f7-button @click="onLazyLoading">Lazy Loading Images</f7-button>
      </p>
    </f7-block>
    <f7-photo-browser
      ref="standalone"
      :photos="photos"
    ></f7-photo-browser>
    <f7-photo-browser
      ref="popup"
      :photos="photos"
      type="popup"
    ></f7-photo-browser>
    <f7-photo-browser
      ref="page"
      :photos="photos"
      type="page"
    ></f7-photo-browser>
    <f7-photo-browser
      ref="darkStandalone"
      theme="dark"
      :photos="photos"
    ></f7-photo-browser>
    <f7-photo-browser
      ref="darkPopup"
      theme="dark"
      :photos="photos"
      type="popup"
    ></f7-photo-browser>
    <f7-photo-browser
      ref="lazyLoading"
      lazyLoading="true"
      theme="dark"
      :photos="photos"
    ></f7-photo-browser>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      photos: [
        {
          url: './static/image/beach.jpg',
          caption: 'Amazing beach in Goa, India'
        }, {
          url: './static/image/1024.jpg',
          caption: ''
        }, {
          url: './static/image/lock.jpg',
          caption: ''
        }, {
          url: './static/image/monkey.jpg',
          caption: 'I met this monkey in Chinese mountains'
        }, {
          url: './static/image/mountains.jpg',
          caption: 'Beautiful mountains in Zhangjiajie, China'
        }
      ]
    }
  },
  methods: {
    onStandalone: function () {
      this.$refs.standalone.open()
    },
    onPopup: function () {
      this.$refs.popup.open()
    },
    onPage: function () {
      this.$refs.page.open()
    },
    onDarkStandalone: function () {
      this.$refs.darkStandalone.open()
    },
    onDarkPopup: function () {
      this.$refs.darkPopup.open()
    },
    onLazyLoading: function () {
      this.$refs.lazyLoading.open()
    }
  }
}
</script>

<style lang="less">

</style>
