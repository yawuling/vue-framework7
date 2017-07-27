<template>
  <f7-page>
    <f7-navbar title="Tabs" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-list>
      <f7-list-item v-for="(item, index) in items"
        media="<i class='icon icon-f7'></i>"
        :title="item.title"
        :link="item.link"
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
          title: 'Static Tabs',
          link: '/tabs/staticTabs/'
        }, {
          title: 'Animated Tabs',
          link: '/tabs/animatedTabs/'
        }, {
          title: 'Swipeable Tabs',
          link: '/tabs/swipeableTabs/'
        }
      ]
    }
  }
}
</script>

<style lang="less">

</style>
