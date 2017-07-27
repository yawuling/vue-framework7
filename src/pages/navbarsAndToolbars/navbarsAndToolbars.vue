<template>
  <f7-page>
    <f7-navbar title="Navbars And Toolbars" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-list>
      <f7-list-item v-for="(item, index) in items"
        link-ignore-cache
        :link="item.link"
        media="<i class='icon icon-f7'></i>"
        :title="item.title"
        :badge="item.badge"
        :badge-color="item.badgeColor"
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
          link: '/navbarsAndToolbars/deepNavbar/',
          title: 'Deep Dynamic Navbar'
        }, {
          link: '/navbarsAndToolbars/hide/',
          title: 'Hide Navbar & Toolbar'
        }, {
          link: '/navbarsAndToolbars/tabbar/',
          title: 'Tab Bar'
        }, {
          link: '/navbarsAndToolbars/tabbarWithLabel/',
          title: 'Tab Bar With Labels'
        }, {
          link: '/navbarsAndToolbars/hideBarsOnScroll/',
          title: 'Hide Bars On Scroll'
        }, {
          link: '/navbarsAndToolbars/subNavbar/',
          title: 'Sub Navbar'
        }, {
          link: '/navbarsAndToolbars/diffScrollTabbar/',
          title: 'Different Scroll Position Tab Bar',
          badge: 'Add',
          badgeColor: 'green'
        }
      ]
    }
  }
}
</script>

<style lang="less">

</style>
