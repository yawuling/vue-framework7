<template>
  <f7-page>
    <f7-navbar title="Hide Navbar & Toolbar" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block inner>
      <p>
        Sometimes you may need to hide top Navbar or bottom Toolbar. Framework7 allows this by adding additional classes to pages. Check examples:
      </p>
    </f7-block>
    <f7-list>
      <f7-list-item v-for="(item, index) in items"
        :link="item.link"
        media="<i class='icon icon-f7'></i>"
        :title="item.title"
        :key="index"
      ></f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          link: '/navbarsAndToolbars/hide/hideNavbar/',
          title: 'Hide Navbar'
        }, {
          link: '/navbarsAndToolbars/hide/hideToolbar/',
          title: 'Hide Toolbar'
        }, {
          link: '/navbarsAndToolbars/hide/hideBoth/',
          title: 'Hide Both'
        }
      ]
    }
  }
}
</script>

<style lang="less">

</style>
