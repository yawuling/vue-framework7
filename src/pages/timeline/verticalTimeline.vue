<template>
  <f7-page>
    <f7-navbar title="Vertical Timeline" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>DEFAULT</f7-block-title>
    <f7-timeline>
      <f7-timeline-item v-for="(item, index) in items1"
        inner
        :day="item.day"
        :month="item.month"
        :content="item.content"
        :key="index"
      ></f7-timeline-item>
    </f7-timeline>
    <f7-block-title>SIDE BY SIDE</f7-block-title>
    <f7-timeline sides>
      <f7-timeline-item v-for="(item, index) in items2"
        inner
        :day="item.day"
        :month="item.month"
        :content="item.content"
        :key="index"
      ></f7-timeline-item>
    </f7-timeline>
    <f7-block-title>ONLY TABLET SIDE BY SIDE</f7-block-title>
    <f7-timeline tablet-sides>
      <f7-timeline-item v-for="(item, index) in items2"
        inner
        :day="item.day"
        :month="item.month"
        :content="item.content"
        :key="index"
      ></f7-timeline-item>
    </f7-timeline>
    <f7-block-title>FORCED SIDES</f7-block-title>
    <f7-timeline sides>
      <f7-timeline-item v-for="(item, index) in items3"
        inner
        :side="item.side"
        :day="item.day"
        :month="item.month"
        :content="item.content"
        :key="index"
      ></f7-timeline-item>
    </f7-timeline>
    <f7-block-title>RICH CONTENT</f7-block-title>
    <f7-timeline>
      <f7-timeline-item day="21" month="DEC" inner>
        <div class="timeline-item-time">12:56</div>
        <div class="timeline-item-title">Item Title</div>
        <div class="timeline-item-subtitle">Item Subtitle</div>
        <div class="timeline-item-text">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor fugiat ipsam hic porro enim, accusamus perferendis, quas commodi alias quaerat eius nemo deleniti. Odio quasi quos quis iure, aperiam pariatur?
        </div>
        <div class="timeline-item-time">15:07</div>
        <div class="timeline-item-title">Item Title</div>
        <div class="timeline-item-subtitle">Item Subtitle</div>
        <div class="timeline-item-text">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor fugiat ipsam hic porro enim, accusamus perferendis, quas commodi alias quaerat eius nemo deleniti. Odio quasi quos quis iure, aperiam pariatur?
        </div>
      </f7-timeline-item>
      <f7-timeline-item day="22" month="DEC">
        <div class="timeline-item-inner">
          <div class="timeline-item-time">12:56</div>
          <div class="timeline-item-title">Item Title</div>
          <div class="timeline-item-subtitle">Item Subtitle</div>
          <div class="timeline-item-text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor fugiat ipsam hic porro enim, accusamus perferendis, quas commodi alias quaerat eius nemo deleniti. Odio quasi quos quis iure, aperiam pariatur?
          </div>
        </div>
        <div class="timeline-item-inner">
          <div class="timeline-item-time">15:07</div>
          <div class="timeline-item-title">Item Title</div>
          <div class="timeline-item-subtitle">Item Subtitle</div>
          <div class="timeline-item-text">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor fugiat ipsam hic porro enim, accusamus perferendis, quas commodi alias quaerat eius nemo deleniti. Odio quasi quos quis iure, aperiam pariatur?
          </div>
        </div>
      </f7-timeline-item>
      <f7-timeline-item day="23" month="DEC" class="timeline-card">
        <f7-card title="Card Header" content="Card Content" footer="Card Footer"></f7-card>  
      </f7-timeline-item>
      <f7-timeline-item day="24" month="DEC" class="timeline-list">
        <f7-list inset>
          <f7-list-item link="#">Item 1</f7-list-item>
          <f7-list-item link="#">Item 1</f7-list-item>
          <f7-list-item link="#">Item 1</f7-list-item>
        </f7-list>
      </f7-timeline-item>
      <f7-timeline-item day="25" month="DEC" content="Plain text"></f7-timeline-item>
    </f7-timeline>
    <f7-block-title>INSIDE CONTENT BLOCK</f7-block-title>
    <f7-block inner>
      <f7-timeline>
        <f7-timeline-item v-for="(item, index) in items1"
          inner
          :day="item.day"
          :month="item.month"
          :content="item.content"
          :key="index"
        ></f7-timeline-item>
      </f7-timeline>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items1: [
        {
          day: '21',
          month: 'DEC',
          content: 'Some text goes here'
        }, {
          day: '22',
          month: 'DEC',
          content: 'Another text goes here'
        }, {
          day: '23',
          month: 'DEC',
          content: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor fugiat ipsam hic porro enim, accusamus perferendis, quas commodi alias quaerat eius nemo deleniti. Odio quasi quos quis iure, aperiam pariatur?'
        }, {
          day: '24',
          month: 'DEC',
          content: 'One more text here'
        }
      ],
      items2: [
        {
          day: '21',
          month: 'DEC',
          content: 'Some text goes here'
        }, {
          day: '22',
          month: 'DEC',
          content: 'Another text goes here'
        }, {
          day: '23',
          month: 'DEC',
          content: 'Just plain text'
        }, {
          day: '24',
          month: 'DEC',
          content: 'One more text here'
        }
      ],
      items3: [
        {
          side: 'right',
          day: '21',
          month: 'DEC',
          content: 'Some text goes here'
        }, {
          side: 'right',
          day: '22',
          month: 'DEC',
          content: 'Another text goes here'
        }, {
          side: 'left',
          day: '23',
          month: 'DEC',
          content: 'Just plain text'
        }, {
          side: 'left',
          day: '24',
          month: 'DEC',
          content: 'One more text here'
        }
      ]
    }
  }
}
</script>

<style lang="less">
.timeline-card{
  .timeline-item-content{
    width: 100%;
  }
}
.timeline-list{
  .timeline-item-content{
    width: 100%;
  }
}
</style>
