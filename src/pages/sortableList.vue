<template>
  <f7-page>
    <f7-navbar title="Sortable List" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link toggle-sortable=".sortable">{{sortable ? 'Done' : 'Edit'}}</f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        Just click "Edit" button on navigation bar to enable sorting
      </p>
    </f7-block>
    <f7-list sortable @sortable:sort="onItemsSort" @sortable:open="onOpen" @sortable:close="onClose">
      <f7-list-item v-for="(item, index) in items"
        media="<i class='icon icon-f7'></i>"
        :title="item.title"
        :after="item.after"
        :key="index"
      ></f7-list-item>
    </f7-list>
    <f7-list media-list sortable>
      <f7-list-item v-for="(item, index) in mediaItems"
        :media="item.media"
        :title="item.title"
        :subtitle="item.subtitle"
        :text="item.text"
        :after="item.after"
        :key="index"
      ></f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      sortable: false,
      items: [
        {
          title: '1 Jenna Smith',
          after: 'CEO'
        }, {
          title: '2 John Doe',
          after: 'Director'
        }, {
          title: '3 John Doe',
          after: 'Developer'
        }, {
          title: '4 Aaron Darling',
          after: 'Manager'
        }, {
          title: '5 Calvin Johnson',
          after: 'Accounter'
        }, {
          title: '6 John Smith',
          after: 'CEO'
        }, {
          title: '7 Chloe',
          after: 'Manager'
        }
      ],
      returnItems: '',   //返回的操作后的数据
      mediaItems: [
        {
          media: '<img src="./static/image/photo1.jpg" width="80" />',
          title: 'Yellow Submarine',
          subtitle: 'Beatles',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '$15'
        }, {
          media: '<img src="./static/image/photo11.jpg" width="80" />',
          title: 'Dont\'t Stop Me Now',
          subtitle: 'Queen',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '$32'
        }, {
          media: '<img src="./static/image/photo6.jpg" width="80" />',
          title: 'Billie Jean',
          subtitle: 'Michael Jackson',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '$16'
        }
      ]
    }
  },
  methods: {
    onOpen: function () {
      this.sortable = !this.sortable
    },
    onClose: function () {
      this.sortable = !this.sortable
    },
    onItemsSort: function (e) {

      //不能对items进行操作，framework7-vue中sortable并没有操作items，而是对Dom树的操作，而v-for是先完成virtual dom的操作再比对操作前的virtual dom树，然后对Dom树只修改变化的部分，而不是重绘

      let startIndex = e.detail.startIndex,
          newIndex = e.detail.newIndex
      
      if (startIndex < newIndex) {
        this.returnItems.splice(newIndex + 1, 0, this.returnItems[startIndex])
        this.returnItems.splice(startIndex, 1)
      } else {
        if (newIndex === 0) {
          this.returnItems.splice(0, 0, this.returnItems[startIndex])
        } else {
          this.returnItems.splice(newIndex, 0, this.returnItems[startIndex])
        }
        this.returnItems.splice(e.detail.startIndex + 1, 1)
      }
    }
  },
  mounted () {
    this.returnItems = this.items.slice(0)
  }
}
</script>

<style lang="less">

</style>
