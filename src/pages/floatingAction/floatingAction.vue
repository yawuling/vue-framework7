<template>
  <f7-page>
    <f7-navbar title="Floating Action Button" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-list>
      <f7-list-item
        media="<i class='icon icon-f7'></i>"
        link="/floatingAction/staticFloating/"
        title="Static Floating Action Button"
        badge="New"
        badge-color="green"
      ></f7-list-item>
      <f7-list-item
        media="<i class='icon icon-f7'></i>"
        link="/floatingAction/speedDial/"
        title="Speed Dial"
        badge="New"
        badge-color="green"
      ></f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less">

</style>
