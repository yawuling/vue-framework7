<template>
  <f7-page>
    <f7-navbar title="Progress Bar" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        In addition to <f7-link href="/preloader/">Preloader</f7-link>, Framework7 also comes with fancy animated determinate and infinite/indeterminate progress bars to indicate some activity.
      </p>
    </f7-block>
    <f7-block-title>DETERMINATE PROGRESS BAR</f7-block-title>
    <f7-block inner>
      <p>
        When progress bar is determinate it indicates how long an operation will take when the percentage complete is detectable.
      </p>
      <p>
        Inline determinate progress bar:
      </p>
      <p>
        <f7-progressbar :progress="10" id="progress1"></f7-progressbar>
      </p>
      <f7-buttons>
        <f7-button @click="setProgress(10)">10%</f7-button>
        <f7-button @click="setProgress(30)">30%</f7-button>
        <f7-button @click="setProgress(50)">50%</f7-button>
        <f7-button @click="setProgress(100)">100%</f7-button>
      </f7-buttons>
      <p>
        Inline determinate load & hide:
      </p>
      <p id="progress-bar-hide"></p>
      <p>
        <f7-button @click="showProgress">Start Loading</f7-button>
      </p>
      <p>
        Overlay with determinate progress bar on top of the app:
      </p>
      <p>
        <f7-button @click="showTopProgress">Start Loading</f7-button>
      </p>
    </f7-block>
    <f7-block-title>INFINITE PROGRESS BAR</f7-block-title>
    <f7-block inner>
      <p>
        When progress bar is infinite/indeterminate it requests that the user wait while something finishes when it’s not necessary to indicate how long it will take.
      </p>
      <p>
        Inline infinite progress bar
      </p>
      <p>
        <f7-progressbar infinite color="blue"></f7-progressbar>
      </p>
      <p>
        Multi-color infinite progress bar
      </p>
      <p>
        <f7-progressbar infinite color="multi"></f7-progressbar>
      </p>
      <p>
        Overlay with infinite progress bar on top of the app
      </p>
      <p>
        <f7-button @click="showTopInfiniteProgress">Start Loading</f7-button>
      </p>
      <p>
        Overlay with infinite multi-color progress bar on top of the app
      </p>
      <p>
        <f7-button @click="showTopInfiniteMulProgress">Start Loading</f7-button>
      </p>
    </f7-block>
    <f7-block-title>COLORED</f7-block-title>
    <f7-list>
      <f7-list-item>
        <f7-progressbar :progress="10" color="blue"></f7-progressbar>
      </f7-list-item>
      <f7-list-item>
        <f7-progressbar :progress="20" color="orange"></f7-progressbar>
      </f7-list-item>
      <f7-list-item>
        <f7-progressbar :progress="30" color="red"></f7-progressbar>
      </f7-list-item>
      <f7-list-item>
        <f7-progressbar :progress="40" color="pink"></f7-progressbar>
      </f7-list-item>
      <f7-list-item>
        <f7-progressbar :progress="50" color="green"></f7-progressbar>
      </f7-list-item>
      <f7-list-item>
        <f7-progressbar :progress="60" color="lightblue"></f7-progressbar>
      </f7-list-item>
      <f7-list-item>
        <f7-progressbar :progress="70" color="yellow"></f7-progressbar>
      </f7-list-item>
      <f7-list-item>
        <f7-progressbar :progress="80" color="gray"></f7-progressbar>
      </f7-list-item>
      <f7-list-item>
        <f7-progressbar :progress="90" color="black"></f7-progressbar>
      </f7-list-item>
      <f7-list-item style="background-color: #999">
        <f7-progressbar :progress="95" color="white"></f7-progressbar>
      </f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      isHide: true,
      isTopHide: true,
      isTopInfiniteHide: true,
      isTopInfiniteMulHide: true
    }
  },
  methods: {
    setProgress: function (data) {
      this.$f7.setProgressbar('#progress1', data)
    },
    showProgress: function () {
      if (!this.isHide) {
        return
      }

      this.$f7.showProgressbar('#progress-bar-hide', 0)
      this.isHide = !this.isHide

      let progress = 0

      this.simulateLoading('#progress-bar-hide', progress, 'isHide')
    },
    simulateLoading: function (container, progress, isHide) {
      let self = this

      setTimeout(function () {
          let progressBefore = progress
          progress += Math.random() * 20
          self.$f7.setProgressbar(container, progress)
          if (progressBefore < 100) {
            self.simulateLoading(container, progress, isHide)
          } else {
            self.$f7.hideProgressbar(container)
            self[isHide] = !self[isHide]
          }
        }, Math.random() * 200 + 200)
    },
    showTopProgress: function () {
      if (!this.isTopHide) {
        return
      }

      this.$f7.showProgressbar('body', 0)
      this.isTopHide = !this.isTopHide

      let progress = 0

      this.simulateLoading('body', progress, 'isTopHide')
    },
    showTopInfiniteProgress: function () {
      let self = this

      if (!self.isTopInfiniteHide) {
        return
      }

      self.$f7.showProgressbar('body')
      self.isTopInfiniteHide = !self.isTopInfiniteHide
      setTimeout(function () {
        self.$f7.hideProgressbar('body')
        self.isTopInfiniteHide = !self.isTopInfiniteHide
      }, 3000)
    },
    showTopInfiniteMulProgress: function () {
      let self = this

      if (!self.isTopInfiniteHide) {
        return
      }

      self.$f7.showProgressbar('body', 'multi')
      self.isTopInfiniteMulHide = !self.isTopInfiniteMulHide
      setTimeout(function () {
        self.$f7.hideProgressbar('body')
        self.isTopInfiniteMulHide = !self.isTopInfiniteMulHide
      }, 3000)
    }
  }
}
</script>

<style lang="less" scoped>
#progress-bar-hide{
  height: 2px;
}
</style>
