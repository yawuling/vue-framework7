<template>
  <f7-page>
    <f7-navbar title="Side Panels" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        Framework7 comes with 2 panels (on left and on right), both are optional. They have two different layouts/effects - <b>cover</b> above the content (like left panel here) and <b>reveal</b> (like right panel). You can put absolutely anything inside: data lists, forms, custom content, and even other isolated app view (like in right panel now) with its own dynamic navbar. Checkout panels:
      </p>
    </f7-block>
    <f7-block>
      <f7-grid>
        <f7-col width="50">
          <f7-button open-panel="left">Left Panel</f7-button>
        </f7-col>
        <f7-col width="50">
          <f7-button open-panel="right">Right Panel</f7-button>
        </f7-col>
      </f7-grid>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less">

</style>
