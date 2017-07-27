<template>
  <f7-page>
    <f7-navbar title="Notifications" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        Framework7 comes with simple Notifications component that allows you to show some useful messages to user.
      </p>
      <p>
        <f7-button @click="onDefault">Default notification</f7-button>
      </p>
      <p>
        <f7-button @click="onFull">Full-layout notification</f7-button>
      </p>
      <p>
        <f7-button @click="onCustom">With custom image</f7-button>
      </p>
      <p>
        <f7-button @click="onCallback">With callback on close</f7-button>
      </p>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  methods: {
    onDefault: function () {
      this.$f7.addNotification({
        title: 'Framework7',
        message: 'This is a simple notification message with title and message'
      })
    },
    onFull: function () {
      this.$f7.addNotification({
        title: 'Framework7',
        subtitle: 'Notification subtitle',
        message: 'This is a simple notification message with custom icon and subtitle',
        media: '<i class="icon icon-f7"></i>'
      })
    },
    onCustom: function () {
      this.$f7.addNotification({
        title: 'My Awesome App',
        subtitle: 'New message from Jhon Doe',
        message: 'Hello, how are you? Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean ut posuere erat. Pellentesque id elementum urna, a aliquam ante. Donec vitae volutpat orci. Aliquam sed molestie risus, quis tincidunt dui.',
        media: '<img width="44" height="44" style="border-radius: 100%" src="./static/image/photo5.jpg" />'
      })
    },
    onCallback: function () {
      let self = this

      self.$f7.addNotification({
        title: 'My Awesome App',
        subtitle: 'New message from Jhon Doe',
        message: 'Hello, how are you? Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean ut posuere erat. Pellentesque id elementum urna, a aliquam ante. Donec vitae volutpat orci. Aliquam sed molestie risus, quis tincidunt dui.',
        media: '<img width="44" height="44" style="border-radius: 100%" src="./static/image/photo5.jpg" />',
        onClose: function () {
          self.$f7.alert('Notification closed')
        }
      })
    }
  }
}
</script>

<style lang="less">

</style>
