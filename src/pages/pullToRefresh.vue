<template>
  <f7-page pull-to-refresh @ptr:refresh="onRefresh">
    <f7-navbar title="Pull To Refresh" back-link="Back" slding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-list media-list>
      <f7-list-item v-for="(item, index) in items"
        :media="item.media"
        :title="item.title"
        :subtitle="item.subtitle"
        :key="index"
      ></f7-list-item>
      <f7-list-label>
        <p>
          <div>Just pull page down to let the magic happen.</div>
          <div>
            Note that pull-to-refresh feature is optimised for touch and native scrolling so it may not work on desktop browser.
          </div>
        </p>
      </f7-list-label>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          media: '<img src="./static/image/photo12.jpg" width="44" />',
          title: 'Yellow Submarie',
          subtitle: 'Beatles'
        }, {
          media: '<img src="./static/image/photo13.jpg" width="44" />',
          title: 'Don\'t Stop Me Now',
          subtitle: 'Queen'
        }, {
          media: '<img src="./static/image/photo14.jpg" width="44" />',
          title: 'Billie Jean',
          subtitle: 'Michael Jackson'
        }
      ]
    }
  },
  methods: {
    onRefresh: function () {
      let self = this

      setTimeout(function () {
        let songs = ['Yellow Submarine', 'Don\'t Stop Me Now', 'Billie Jean', 'Californication'],
            authors = ['Beatles', 'Queen', 'Michael Jackson', 'Red Hot Chili Peppers']
        let item = {
          media: '<img src="./static/image/photo' + Math.floor(Math.random() * 14) + '.jpg" width="44" />',
          title: songs[Math.floor(Math.random() * songs.length)],
          subtitle: authors[Math.floor(Math.random() * authors.length)]
        }

        self.items.unshift(item)

        self.$f7.pullToRefreshDone()
      }, 2000)
    }
  }
}
</script>

<style lang="less">

</style>
