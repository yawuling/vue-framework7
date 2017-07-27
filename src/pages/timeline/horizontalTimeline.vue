<template>
  <f7-page name="horizontal-timeline">
    <f7-navbar title="Horizontal Timeline" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-timeline horizontal col="33" tablet-col="20">
      <f7-timeline-item v-for="item in items"
        :day="item.day"
        :month="item.month"
        :content="item.content"
        :key="item.day"
      >
        <template v-if="item.card">
          <f7-card v-for="(child, index) in item.children"
            :title="child.cardHeader"
            :content="child.cardContent"
            :footer="child.cardFooter"
            :key="index"
          ></f7-card>
        </template>
        <template v-else-if="item.list">
          <f7-list v-for="(child, index) in item.children" :inset="child.inset" :key="index">
            <f7-list-item v-for="list in child.lists" :title="list.title" :link="list.link" :key="list.title"></f7-list-item>
          </f7-list>
        </template>
        <template v-else>
          <f7-timeline-item-child v-for="(child, index) in item.children"
            :inner="child.inner"
            :time="child.time"
            :title="child.title"
            :subtitle="child.subtitle"
            :text="child.text"
            :key="index"
          ></f7-timeline-item-child>
        </template>
      </f7-timeline-item>
    </f7-timeline>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          day: '21',
          month: 'DEC',
          children: [
            {
              time: '12:56',
              title: 'Title 1',
              subtitle: 'Subtitle 1',
              text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit',
              inner: true
            }, {
              time: '13:15',
              title: 'Title 2',
              subtitle: 'Subtitle 2',
              text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit',
              inner: true
            }, {
              time: '14:45',
              text: 'Do something',
              inner: true
            }, {
              time: '16:11',
              text: 'Do something else',
              inner: true
            }
          ]
        }, {
          day: '22',
          month: 'DEC',
          content: 'Plain text goes here'
        }, {
          day: '23',
          month: 'DEC',
          card: true,
          children: [
            {
              cardHeader: 'Card',
              cardContent: 'Card Content',
              cardFooter: 'Card Footer'
            }, {
              cardContent: 'Another Card'
            }
          ]
        }, {
          day: '24',
          month: 'DEC',
          list: true,
          children: [
            {
              inset: true,
              lists: [
                {
                  title: 'Item 1',
                  link: '#'
                }, {
                  title: 'Item 2',
                  link: '#'
                }, {
                  title: 'Item 3',
                  link: '#'
                }
              ]
            }
          ]
        }, {
          day: '25',
          month: 'DEC',
          children: [
            {
              time: '11:11',
              text: 'Task 1',
              inner: false
            }, {
              time: '12:33',
              text: 'Task 2',
              inner: false
            }, {
              time: '13:24',
              text: 'Task 3',
              inner: false
            }, {
              time: '14:55',
              text: 'Task 4',
              inner: false
            }, {
              time: '15:15',
              text: 'Task 5',
              inner: false
            }, {
              time: '16:54',
              text: 'Task 6',
              inner: false
            }
          ]
        }, {
          day: '26',
          month: 'DEC',
          children: [
            {
              time: '11:11',
              text: 'Task 1',
              inner: true
            }, {
              time: '12:33',
              text: 'Task 2',
              inner: true
            }, {
              time: '13:24',
              text: 'Task 3',
              inner: true
            }, {
              time: '14:55',
              text: 'Task 4',
              inner: true
            }, {
              time: '15:15',
              text: 'Task 5',
              inner: true
            }, {
              time: '16:54',
              text: 'Task 6',
              inner: true
            }
          ]
        }
      ]
    }
  }
}
</script>

<style lang="less">
.page[data-page="horizontal-timeline"]{
  .timeline-item-child{
    margin-top: 15px;

    &:first-child{
      margin-top: 0;
    }
  }
}
</style>
