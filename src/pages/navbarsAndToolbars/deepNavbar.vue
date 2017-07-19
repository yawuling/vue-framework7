<template>
  <f7-page>
    <f7-navbar>
      <f7-nav-left sliding>
         <f7-link back>Navbars</f7-link> 
      </f7-nav-left>
      <f7-nav-center sliding>Deep Navbar</f7-nav-center>
      <f7-nav-right sliding>
        <f7-link href="/navbarsAndToolbars/deepNavbar/deep2/">Deep 2</f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <div class="content-block-inner">
        <p>
          This demo demonstrates Framework7 exclusive behavior of dynamic sliding navigation bars. Just click the button below and look how navbar links will change. And don't forget to try swipe-back gesture on next pages:
        </p>
      </div>
      <p><f7-button href="/navbarsAndToolbars/deepNavbar/deep2/">Go to page 2</f7-button></p>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less">

</style>
