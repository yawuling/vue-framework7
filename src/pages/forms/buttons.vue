<template>
  <f7-page>
    <f7-navbar title="Buttons" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>USUAL BUTTONS</f7-block-title>
    <f7-block>
      <f7-grid>
        <f7-col>
          <f7-button active>Active</f7-button>
        </f7-col>
        <f7-col>
          <f7-button>Button</f7-button>
        </f7-col>
        <f7-col>
          <f7-button round>Round</f7-button>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block>
      <f7-grid>
        <f7-col>
          <f7-button active>Active</f7-button>
        </f7-col>
        <f7-col>
          <f7-button>Button</f7-button>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block>
      <f7-buttons>
        <f7-button>Button</f7-button>
        <f7-button>Button</f7-button>
      </f7-buttons>
    </f7-block>
    <f7-block>
      <f7-buttons>
        <f7-button round>Button</f7-button>
        <f7-button round>Button</f7-button>
        <f7-button round>Button</f7-button>
      </f7-buttons>
    </f7-block>
    <f7-block>
      <f7-buttons>
        <f7-button>Button</f7-button>
        <f7-button active>Button</f7-button>
        <f7-button>Button</f7-button>
        <f7-button>Button</f7-button>
      </f7-buttons>
    </f7-block>
    <f7-block-title>BIG BUTTONS</f7-block-title>
    <f7-block>
      <f7-grid>
        <f7-col>
          <f7-button big active>Active</f7-button>
        </f7-col>
        <f7-col>
          <f7-button big>Button</f7-button>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block-title>THEMED FILL BUTTONS</f7-block-title>
    <f7-block>
      <f7-grid>
        <f7-col>
          <f7-button big fill color="green">Submit</f7-button>
        </f7-col>
        <f7-col>
          <f7-button big fill color="red">Cancel</f7-button>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block-title>LIST-BLOCK BUTTONS</f7-block-title>
    <f7-list inset>
      <f7-list-button>List Button 1</f7-list-button>
      <f7-list-button>List Button 2</f7-list-button>
      <f7-list-button>List Button 3</f7-list-button>
    </f7-list>
    <f7-list inset>
      <f7-list-button color="red">List Button 1</f7-list-button>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less">

</style>
