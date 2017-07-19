<template>
  <f7-page>
    <f7-navbar title="Grid" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>Framework7 comes with flexible layout grid:</f7-block>
    <f7-block-title>COLUMNS WITH GUTTER</f7-block-title>
    <f7-block class="ks-grid">
      <f7-grid>
        <f7-col width="50">.col-50</f7-col>
        <f7-col width="50">.col-50</f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="25">.col-25</f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="33">.col-33</f7-col>
        <f7-col width="33">.col-33</f7-col>
        <f7-col width="33">.col-33</f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="20">.col-20</f7-col>
        <f7-col width="20">.col-20</f7-col>
        <f7-col width="20">.col-20</f7-col>
        <f7-col width="20">.col-20</f7-col>
        <f7-col width="20">.col-20</f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="33">.col-33</f7-col>
        <f7-col width="66">.col-66</f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="50">.col-50</f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="75">.col-75</f7-col>
        <f7-col width="25">.col-25</f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="80">.col-80</f7-col>
        <f7-col width="20">.col-20</f7-col>
      </f7-grid>
    </f7-block>
    <f7-block-title>NO GUTTER BETWEEN COLUMNS</f7-block-title>
    <f7-block class="ks-grid">
      <f7-grid no-gutter>
        <f7-col width="50">.col-50</f7-col>
        <f7-col width="50">.col-50</f7-col>
      </f7-grid>
      <f7-grid no-gutter>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="25">.col-25</f7-col>
      </f7-grid>
      <f7-grid no-gutter>
        <f7-col width="33">.col-33</f7-col>
        <f7-col width="33">.col-33</f7-col>
        <f7-col width="33">.col-33</f7-col>
      </f7-grid>
      <f7-grid no-gutter>
        <f7-col width="20">.col-20</f7-col>
        <f7-col width="20">.col-20</f7-col>
        <f7-col width="20">.col-20</f7-col>
        <f7-col width="20">.col-20</f7-col>
        <f7-col width="20">.col-20</f7-col>
      </f7-grid>
      <f7-grid no-gutter>
        <f7-col width="33">.col-33</f7-col>
        <f7-col width="66">.col-66</f7-col>
      </f7-grid>
      <f7-grid no-gutter>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="25">.col-25</f7-col>
        <f7-col width="50">.col-50</f7-col>
      </f7-grid>
      <f7-grid no-gutter>
        <f7-col width="75">.col-75</f7-col>
        <f7-col width="25">.col-25</f7-col>
      </f7-grid>
      <f7-grid no-gutter>
        <f7-col width="80">.col-80</f7-col>
        <f7-col width="20">.col-20</f7-col>
      </f7-grid>
    </f7-block>
    <f7-block-title>NESTED</f7-block-title>
    <f7-block class="ks-grid">
      <f7-grid>
        <f7-col width="50">
          <f7-grid>
            <f7-col width="50">.col-50</f7-col>
            <f7-col width="50">.col-50</f7-col>
          </f7-grid>
        </f7-col>
        <f7-col width="50">
          <f7-grid>
            <f7-col width="33">.col-33</f7-col>
            <f7-col width="66">.col-66</f7-col>
          </f7-grid>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block-title>RESPONSIVE GRID</f7-block-title>
    <f7-block class="ks-grid">
      <p>Grid cells have different size on Phone/Tablet</p>
      <f7-grid>
        <f7-col width="100" tablet-width="50">.col-100.tablet-50</f7-col>
        <f7-col width="100" tablet-width="50">.col-100.tablet-50</f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="50" tablet-width="25">.col-50.tablet-25</f7-col>
        <f7-col width="50" tablet-width="25">.col-50.tablet-25</f7-col>
        <f7-col width="50" tablet-width="25">.col-50.tablet-25</f7-col>
        <f7-col width="50" tablet-width="25">.col-50.tablet-25</f7-col>
      </f7-grid>
      <f7-grid>
        <f7-col width="100" tablet-width="40">.col-100.tablet-40</f7-col>
        <f7-col width="50" tablet-width="60">.col-50.tablet-60</f7-col>
        <f7-col width="50" tablet-width="66">.col-50.tablet-66</f7-col>
        <f7-col width="100" tablet-width="33">.col-100.tablet-33</f7-col>
      </f7-grid>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less" scoped>
.ks-grid{
  div[class*="col-"] {
    background: #fff;
    text-align: center;
    color: #000;
    border: 1px solid #ddd;
    padding: 5px;
    margin-bottom: 15px;
  }
}
</style>
