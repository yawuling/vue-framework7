<template>
  <f7-page no-toolbar>
    <f7-navbar title="Hide Toolbar" back-link="Back">
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <div class="content-block-inner">
        <p>
          On this page Toolbar was hidden dynamically. Just add "no-toolbar" class to this page to make it work.
        </p>
      </div>
      <p>
        <f7-button back>Go Back</f7-button>
      </p>
    </f7-block>
  </f7-page>
</template>
