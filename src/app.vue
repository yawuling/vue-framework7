<template>
  <!-- App -->
  <div id="app">

    <!-- Statusbar -->
    <f7-statusbar></f7-statusbar>

    <!-- Left Panel -->
    <f7-panel left cover layout="dark">
      <f7-view id="left-panel-view" navbar-through :dynamic-navbar="true">
        <f7-navbar v-if="$theme.ios" title="Left Panel" sliding></f7-navbar>
        <f7-pages>
          <f7-page>
            <f7-navbar v-if="$theme.material" title="Left Panel" sliding></f7-navbar>
            <f7-block inner>
              <p>Left panel content goes here</p>
            </f7-block>
            <f7-block-title>Load page in panel</f7-block-title>
            <f7-list>
              <f7-list-item link="/about/" title="About"></f7-list-item>
              <f7-list-item link="/form/" title="Form"></f7-list-item>
            </f7-list>
            <f7-block-title>Load page in main view</f7-block-title>
            <f7-list>
              <f7-list-item link="/about/" title="About" link-view="#main-view" link-close-panel></f7-list-item>
              <f7-list-item link="/form/" title="Form" link-view="#main-view" link-close-panel></f7-list-item>
            </f7-list>
          </f7-page>
        </f7-pages>
      </f7-view>
    </f7-panel>

    <!-- Main Views -->
    <f7-views>
      <f7-view id="main-view" navbar-through toolbar-through :dynamic-navbar="true" main>
        <!-- iOS Theme Navbar -->
        <f7-navbar v-if="$theme.ios">
          <f7-nav-center sliding>Framework7</f7-nav-center>
          <f7-nav-right>
            <f7-link icon="icon-bars" open-panel="left"></f7-link>
          </f7-nav-right>
        </f7-navbar>
        <!-- Pages -->
        <f7-pages>
          <main-page></main-page>
        </f7-pages>
        <!-- IOS Theme Toolbar -->
        <f7-toolbar v-if="$theme.ios">
          <f7-link>Dummy Link</f7-link>
          <f7-link>Menu</f7-link>
        </f7-toolbar>
      </f7-view>
    </f7-views>

    <!-- Login Screen -->
    <f7-login-screen id="login-screen">
      <f7-view>
        <f7-pages>
           <f7-page login-screen>
            <f7-login-screen-title>Framework7</f7-login-screen-title>
            <f7-list form>
              <f7-list-item>
                <f7-label>Username</f7-label>
                <f7-input name="username" placeholder="Your username" type="text" v-model="username"></f7-input>
              </f7-list-item>
              <f7-list-item>
                <f7-label>Password</f7-label>
                <f7-input name="password" type="password" placeholder="Your password" v-model="password"></f7-input>
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
        </f7-pages>
      </f7-view>
    </f7-login-screen>
  </div>
</template>

<script>
import MainPage from './pages/mainPage.vue'

export default {
  data () {
    return {
      username: '',
      password: ''
    }
  },
  components: { MainPage },
  methods: {
    closeLogin: function () {
      let loginText = 'Username:' + this.username + ',password:' + this.password
      this.$f7.alert(loginText, 'Framework7', function () {
        window.f7.closeModal('#login-screen')
      })
    }
  }
}
</script>

<style lang="less">
  html.ios-gt-8 .navbar .center{
    font-weight: 500;
  }
</style>
