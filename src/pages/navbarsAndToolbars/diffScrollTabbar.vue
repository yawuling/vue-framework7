<template>
  <f7-page no-toolbar toolbar-fixed tabs no-page-content data-page="toolbar">
    <f7-navbar title="Diff Scroll Tab Bar" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-toolbar tabbar labels>
      <f7-link
        tab-link="#tab1"
        no-link-class
        active>
        <f7-icon f7="help" class="inactive"></f7-icon>
        <f7-icon f7="help_fill" class="active"></f7-icon>
        <span class="tabbar-label">Information</span>
      </f7-link>
      <f7-link
        tab-link="#tab2"
        no-link-class>
        <f7-icon f7="drawers" class="inactive">
          <f7-badge color="red">9</f7-badge>
        </f7-icon>
        <f7-icon f7="drawers_fill" class="active">
          <f7-badge color="red">9</f7-badge>
        </f7-icon>
        <span class="tabbar-label">Inbox</span>
      </f7-link>
      <f7-link
        tab-link="#tab3"
        no-link-class>
        <f7-icon f7="cloud" class="inactive"></f7-icon>  
        <f7-icon f7="cloud_fill" class="active"></f7-icon>
        <span class="tabbar-label">Upload</span>
      </f7-link>
      <f7-link
        tab-link="#tab4"
        no-link-class>
        <f7-icon f7="camera" class="inactive"></f7-icon>
        <f7-icon f7="camera_fill" class="active"></f7-icon>
        <span class="tabbar-label">Photos</span>
      </f7-link>
    </f7-toolbar>
    <f7-page-content tab active id="tab1"><tab1></tab1></f7-page-content>
    <f7-page-content tab id="tab2"><tab2></tab2></f7-page-content>
    <f7-page-content tab id="tab3"><tab3></tab3></f7-page-content>
    <f7-page-content tab id="tab4"><tab4></tab4></f7-page-content>
  </f7-page>
</template>

<script>
import Tab1 from './tab1'
import Tab2 from './tab2'
import Tab3 from './tab3'
import Tab4 from './tab4'

export default {
  components: { Tab1, Tab2, Tab3, Tab4 }
}
</script>

<style lang="less">
.page[data-page="toolbar"]{
  .toolbar{
    transform: none;
    transition: 0ms;

    a.active{
      i.inactive{
        display: none;
      }
      i.active{
        margin-left: 0;
        color: #007aff;
      }
    }
  }
  .tabbar{
    a:not(.active){
      i.active{
        display: none;
      }
    }
  }
}
</style>
