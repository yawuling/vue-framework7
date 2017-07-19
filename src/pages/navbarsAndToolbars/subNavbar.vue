<template>
  <f7-page hide-bars-on-scroll with-subnavbar>
    <f7-navbar title="Sub Navbar" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
      <f7-subnavbar sliding>
        <f7-buttons>
          <f7-button active>Link 1</f7-button>
          <f7-button>Link 2</f7-button>
          <f7-button>Link 3</f7-button>
          <f7-button>Link 4</f7-button>
        </f7-buttons>
      </f7-subnavbar>
    </f7-navbar>
    <f7-block>
      Sub Navbar is useful when you need to put any additional elements into Navbar, like Tab Links or Search Bar. It also remains visible when Navbar hidden.
    </f7-block>
    <f7-block>
      <p v-for="item in items">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse at luctus dui. Praesent venenatis libero orci, in scelerisque enim tincidunt eget. Pellentesque id odio id enim consectetur condimentum. Maecenas dapibus tempus diam. Suspendisse cursus, est ut feugiat tempus, lectus odio aliquam dui, non suscipit lectus sapien vitae velit. Vestibulum tempus faucibus massa, et rutrum odio luctus finibus. Praesent aliquet accumsan magna, quis ornare elit scelerisque sit amet. Mauris commodo varius velit dictum dictum. Sed non sapien urna. Nunc porta vitae massa nec rutrum. Praesent et porttitor tortor, vitae tristique nibh. Morbi sed tempor tellus, sit amet pharetra ante. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Duis porta feugiat nisl sed blandit.
      </p>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items: 9
    }
  }
}
</script>

<style lang="less">

</style>
