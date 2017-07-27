<template>
  <f7-page>
    <f7-navbar title="Animation" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block inner>
      <p>
        Framework7 comes with own simple and fast animation helper library to create custom JS animations:
      </p>
      <p>
        <f7-button @click="startAnimate">Animate</f7-button>
      </p>
      <div id="animate-me" style="width: 100px; height: 100px; margin-left: 0px; margin-top: 0px;" class="bg-red"></div>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  methods: {
    startAnimate: function () {
      let self = this

      self.$$('#animate-me')
        .animate(
          {
            'width': 200,
            'height': 50,
            'margin-left': 50,
            'margin-top': 0,
          }, {
            duration: 600,
            easing: 'swing'
          }
        )
        .animate(
          {
            'width': 50,
            'height': 200,
            'margin-left': 0,
            'margin-top': 50,
          }, {
            duration: 600,
            easing: 'swing'
          }
        )
        .animate(
          {
            'width': 100,
            'height': 100,
            'margin-left': 0,
            'margin-top': 0,
          }, {
            duration: 600,
            easing: 'swing',
            complete: function () {
              self.$f7.alert('Animation completed');
            }
          }
        );
    }
  }
}
</script>

<style lang="less">

</style>
