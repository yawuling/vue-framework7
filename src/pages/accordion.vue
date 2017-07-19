<template>
  <f7-page>
    <f7-navbar title="Accordion" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>LIST VIEW ACCORDION</f7-block-title>
    <f7-list accordion>
      <f7-list-item accordion-item title="Lorem Ipsum">
        <f7-accordion-content>
          <f7-block>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean elementum id neque nec commodo. Sed vel justo at turpis laoreet pellentesque quis sed lorem. Integer semper arcu nibh, non mollis arcu tempor vel. Sed pharetra tortor vitae est rhoncus, vel congue dui sollicitudin. Donec eu arcu dignissim felis viverra blandit suscipit eget ipsum.
            </p>
          </f7-block>
        </f7-accordion-content>
      </f7-list-item>
      <f7-list-item accordion-item title="Nested List">
        <f7-accordion-content>
          <f7-list>
            <f7-list-item media="<i class='icon icon-f7'></i>" title="Item 1"></f7-list-item>
            <f7-list-item media="<i class='icon icon-f7'></i>" title="Item 2"></f7-list-item>
            <f7-list-item media="<i class='icon icon-f7'></i>" title="Item 3"></f7-list-item>
            <f7-list-item media="<i class='icon icon-f7'></i>" title="Item 4"></f7-list-item>
          </f7-list>
        </f7-accordion-content>
      </f7-list-item>
      <f7-list-item accordion-item title="Integer semper">
        <f7-accordion-content>
          <f7-block>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean elementum id neque nec commodo. Sed vel justo at turpis laoreet pellentesque quis sed lorem. Integer semper arcu nibh, non mollis arcu tempor vel. Sed pharetra tortor vitae est rhoncus, vel congue dui sollicitudin. Donec eu arcu dignissim felis viverra blandit suscipit eget ipsum.
            </p>
          </f7-block>
        </f7-accordion-content>
      </f7-list-item>
    </f7-list>
    <f7-block-title>INSET ACCORDION</f7-block-title>
    <f7-list accordion inset>
      <f7-list-item accordion-item title="Lorem Ipsum">
        <f7-accordion-content>
          <f7-block>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean elementum id neque nec commodo. Sed vel justo at turpis laoreet pellentesque quis sed lorem. Integer semper arcu nibh, non mollis arcu tempor vel. Sed pharetra tortor vitae est rhoncus, vel congue dui sollicitudin. Donec eu arcu dignissim felis viverra blandit suscipit eget ipsum.
            </p>
          </f7-block>
        </f7-accordion-content>
      </f7-list-item>
      <f7-list-item accordion-item title="Nested List">
        <f7-accordion-content>
          <f7-list>
            <f7-list-item media="<i class='icon icon-f7'></i>" title="Item 1"></f7-list-item>
            <f7-list-item media="<i class='icon icon-f7'></i>" title="Item 2"></f7-list-item>
            <f7-list-item media="<i class='icon icon-f7'></i>" title="Item 3"></f7-list-item>
            <f7-list-item media="<i class='icon icon-f7'></i>" title="Item 4"></f7-list-item>
          </f7-list>
        </f7-accordion-content>
      </f7-list-item>
      <f7-list-item accordion-item title="Integer semper">
        <f7-accordion-content>
          <f7-block>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean elementum id neque nec commodo. Sed vel justo at turpis laoreet pellentesque quis sed lorem. Integer semper arcu nibh, non mollis arcu tempor vel. Sed pharetra tortor vitae est rhoncus, vel congue dui sollicitudin. Donec eu arcu dignissim felis viverra blandit suscipit eget ipsum.
            </p>
          </f7-block>
        </f7-accordion-content>
      </f7-list-item>
    </f7-list>
    <f7-block-title>CUSTOM STYLED ACCORDION</f7-block-title>
    <f7-accordion class="custom-accordion">
      <f7-accordion-item>
        <f7-accordion-toggle>
          <i class="icon icon-plus">+</i>
          <i class="icon icon-minus">-</i>
          <span>Item 1</span>
        </f7-accordion-toggle>
        <f7-accordion-content>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean elementum id neque nec commodo. Sed vel justo at turpis laoreet pellentesque quis sed lorem. Integer semper arcu nibh, non mollis arcu tempor vel. Sed pharetra tortor vitae est rhoncus, vel congue dui sollicitudin. Donec eu arcu dignissim felis viverra blandit suscipit eget ipsum.
          </p>
        </f7-accordion-content>
      </f7-accordion-item>
      <f7-accordion-item>
        <f7-accordion-toggle>
          <i class="icon icon-plus">+</i>
          <i class="icon icon-minus">-</i>
          <span>Item 2</span>
        </f7-accordion-toggle>
        <f7-accordion-content>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean elementum id neque nec commodo. Sed vel justo at turpis laoreet pellentesque quis sed lorem. Integer semper arcu nibh, non mollis arcu tempor vel. Sed pharetra tortor vitae est rhoncus, vel congue dui sollicitudin. Donec eu arcu dignissim felis viverra blandit suscipit eget ipsum.
          </p>
        </f7-accordion-content>
      </f7-accordion-item>
      <f7-accordion-item>
        <f7-accordion-toggle>
          <i class="icon icon-plus">+</i>
          <i class="icon icon-minus">-</i>
          <span>Item 3</span>
        </f7-accordion-toggle>
        <f7-accordion-content>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean elementum id neque nec commodo. Sed vel justo at turpis laoreet pellentesque quis sed lorem. Integer semper arcu nibh, non mollis arcu tempor vel. Sed pharetra tortor vitae est rhoncus, vel congue dui sollicitudin. Donec eu arcu dignissim felis viverra blandit suscipit eget ipsum.
          </p>
        </f7-accordion-content>
      </f7-accordion-item>
    </f7-accordion>
  </f7-page>
</template>

<script>
export default {
}
</script>

<style lang="less" scoped>
.custom-accordion{
  .accordion-item-toggle{
    padding: 0 15px;
    height: 44px;
    line-height: 44px;
    font-size: 17px;
    color: #000;
    border-bottom: 1px solid rgba(0, 0, 0, 0.15);
    cursor: pointer;

    .icon{
      border: 1px solid #000;
      border-radius: 100%;
      width: 25px;
      height: 25px;
      font-size: 31px;
      line-height: 20px;
      text-align: center;
      font-weight: 100;
    }

    span{
      margin-left: 15px;
    }
  }
  .accordion-item-content{
    padding: 0 15px;

    p{
      color: #6d6d72;
    }
  }
}
.custom-accordion .accordion-item-expanded{
  .icon-plus{
    display: none;
  }
  .icon-minus{
    display: inline-block;
  }
}

.custom-accordion .icon-minus{
  display: none;
}
</style>
