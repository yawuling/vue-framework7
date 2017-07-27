<template>
  <f7-page>
    <f7-navbar title="Timeline" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-list>
      <f7-list-item v-for="(item, index) in items"
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
          title: 'Vertical Timeline',
          link: '/timeline/verticalTimeline/'
        }, {
          title: 'Horizontal Timeline',
          link: '/timeline/horizontalTimeline/'
        }, {
          title: 'Calendar Timeline',
          link: '/timeline/calendarTimeline/'
        }
      ]
    }
  }
}
</script>

<style lang="less">

</style>
