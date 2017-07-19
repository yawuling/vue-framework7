<template>
  <f7-page no-navbar no-toolbar no-swipeback login-screen>
    <f7-login-screen-title>Framework7</f7-login-screen-title>
    <f7-list form>
      <f7-list-item>
        <f7-label>Username</f7-label>
        <f7-input name="username" placeholder="Your username" type="text" v-modal="username"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Password</f7-label>
        <f7-input name="password" type="password" placeholder="Your password" v-modal="username"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-list>
      <f7-list-button title="Sign In" @click="closeLogin"></f7-list-button>
      <f7-list-label>
        <div>Some text about login information.</div>
        <div>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</div>
      </f7-list-label>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    closeLogin: function () {
      let self = this
      let loginText = 'Username:' + this.username + ',password:' + this.password
      this.$f7.alert(loginText, 'Framework7', function () {
        self.$router.back()
      })
    }
  }
}
</script>

<style lang="less">

</style>
