<template>
  <f7-page toolbar-fixed no-toolbar data-page="toolbar">
    <f7-navbar title="Tab Bar With Labels" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-toolbar tabbar labels>
      <f7-link
        route-tab-link="#tab1"
        href="/navbarsAndToolbars/tabbarWithLabel/">
        <f7-icon f7="help" class="inactive"></f7-icon>
        <f7-icon f7="help_fill" class="active"></f7-icon>
        <span class="tabbar-label">Information</span>
      </f7-link>
      <f7-link
        route-tab-link="#tab2"
        href="/navbarsAndToolbars/tabbarWithLabel/tab2/">
        <f7-icon f7="drawers" class="inactive">
          <f7-badge color="red">4</f7-badge>
        </f7-icon>
        <f7-icon f7="drawers_fill" class="active">
          <f7-badge color="red">4</f7-badge>
        </f7-icon>
        <span class="tabbar-label">Inbox</span>
      </f7-link>
      <f7-link
        route-tab-link="#tab3"
        href="/navbarsAndToolbars/tabbarWithLabel/tab3/">
        <f7-icon f7="cloud" class="inactive"></f7-icon>  
        <f7-icon f7="cloud_fill" class="active"></f7-icon>
        <span class="tabbar-label">Upload</span>
      </f7-link>
      <f7-link
        route-tab-link="#tab4"
        href="/navbarsAndToolbars/tabbarWithLabel/tab4/">
        <f7-icon f7="camera" class="inactive"></f7-icon>
        <f7-icon f7="camera_fill" class="active"></f7-icon>
        <span class="tabbar-label">Photos</span>
      </f7-link>
    </f7-toolbar>
    <f7-tabs>
      <f7-tab id="tab1"></f7-tab>
      <f7-tab id="tab2"></f7-tab>
      <f7-tab id="tab3"></f7-tab>
      <f7-tab id="tab4"></f7-tab>
    </f7-tabs>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less">
.page[data-page="toolbar"]{
  .page-content{
    padding-bottom: 44px;
  }
  .toolbar{
    transform: none;
    transition: 0ms;

    .active-state{
      opacity: 1;
      transition: 0ms;
    }
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
