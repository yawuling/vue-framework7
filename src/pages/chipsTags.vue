<template>
  <f7-page>
    <f7-navbar title="Chips/Tags" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>Chips/Tags represent complex entities in small blocks, such as a contact. They can contain a photo, short title string, and brief information.</f7-block>
    <f7-block-title>CHIPS WITH TEXT</f7-block-title>
    <f7-block inner>
      <f7-chip text="Example Chip"></f7-chip>
      <f7-chip text="Another Chip"></f7-chip>
      <f7-chip text="One More Chip"></f7-chip>
      <f7-chip text="Fourth Chip"></f7-chip>
      <f7-chip text="Last One"></f7-chip>
    </f7-block>
    <f7-block-title>ICON CHIPS</f7-block-title>
    <f7-block inner>
      <f7-chip media="<i class='icon f7-icons'>add_round</i>" text="Add Contact"></f7-chip>
      <f7-chip media="<i class='icon f7-icons'>compass</i>" text="London"></f7-chip>
      <f7-chip media="<i class='icon f7-icons'>person</i>" text="John Doe"></f7-chip>
    </f7-block>
    <f7-block-title>CONTACT CHIPS</f7-block-title>
    <f7-block inner>
      <f7-chip media="<img src='./static/image/photo5.jpg'>" text="John Doe"></f7-chip>
      <f7-chip media="<img src='./static/image/photo6.jpg'>" text="John Doe"></f7-chip>
      <f7-chip media="<img src='./static/image/photo7.jpg'>" text="Adam Smith"></f7-chip>
      <f7-chip media="J" media-bg="pink" text="Jennifer"></f7-chip>
      <f7-chip media="C" media-bg="yellow" media-color="black" text="Chris"></f7-chip>
      <f7-chip media="K" media-bg="red" text="Kate"></f7-chip>
    </f7-block>
    <f7-block-title>DELETABLE CHIPS / TAGS</f7-block-title>
    <f7-block inner>
      <f7-chip text="Example Chip" deleteable></f7-chip>
      <f7-chip media="C" media-bg="yellow" media-color="black" text="Chris" deleteable></f7-chip>
      <f7-chip media="<img src='./static/image/photo5.jpg'>" text="John Doe" deleteable></f7-chip>
      <f7-chip text="One More Chip" deleteable></f7-chip>
      <f7-chip media="J" media-bg="pink" text="Jennifer" deleteable></f7-chip>
      <f7-chip media="<img src='./static/image/photo6.jpg'>" text="John Doe" deleteable></f7-chip>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less">

</style>
