<template>
  <f7-page>
    <f7-navbar title="Login Screen" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>Framework7 comes with ready to use Login Screen layout. It could be used inside of page or inside of popup (Embedded) or as a standalone overlay:</f7-block>
    <f7-block>
      <f7-grid>
        <f7-col width="50">
          <f7-button href="/loginScreen/loginScreenEmbedded/">Embedded into Page</f7-button>
        </f7-col>
        <f7-col width="50">
          <f7-button open-popup="#login-screen">As Overlay</f7-button>
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
