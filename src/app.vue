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
      <f7-view id="main-view" navbar-through :dynamic-navbar="true" main>
        <!-- iOS Theme Navbar -->
        <f7-navbar v-if="$theme.ios">
          <f7-nav-center sliding>Framework7</f7-nav-center>
          <f7-nav-right>
            <f7-link icon="icon-bars" open-panel="left"></f7-link>
          </f7-nav-right>
        </f7-navbar>
        <!-- Pages -->
        <f7-pages>
          <f7-page>
            <!-- Material Theme Navbar -->
            <f7-navbar v-if="$theme.material">
              <f7-nav-center sliding>Framework7</f7-nav-center>
              <f7-nav-right>
                <f7-link icon="icon-bars" open-panel="right"></f7-link>
              </f7-nav-right>
            </f7-navbar>
            <!-- Page Content -->
            <f7-block-title>Welcome to Framework7</f7-block-title>
            <f7-block>
              <f7-button href="/about/">About Framework7</f7-button>
            </f7-block>
            <f7-block-title>FRAMEWORK7 KITCHEN SINK</f7-block-title>
            <f7-list v-for="list in lists">
              <f7-list-item v-for="item in list"
                  media="<i class='icon icon-f7'></i>"
                  :link="item.link"
                  :title="item.title"
                  :badge="item.badge"
                  :badge-color="item.badgeColor"
              ></f7-list-item>
            </f7-list>
          </f7-page>
        </f7-pages>
      </f7-view>
    </f7-views>

    <!-- Popup -->
    <f7-popup id="popup">
      <f7-view navbar-fixed>
        <f7-pages>
          <f7-page>
            <f7-navbar title="Popup">
              <f7-nav-right>
                <f7-link close-popup>Close</f7-link>
              </f7-nav-right>
            </f7-navbar>
            <f7-block>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Neque, architecto. Cupiditate laudantium rem nesciunt numquam, ipsam. Voluptates omnis, a inventore atque ratione aliquam. Omnis iusto nemo quos ullam obcaecati, quod.</f7-block>
          </f7-page>
        </f7-pages>
      </f7-view>
    </f7-popup>

    <!-- Login Screen -->
    <f7-login-screen id="login-screen">
      <f7-view>
        <f7-pages>
          <f7-page login-screen>
            <f7-login-screen-title>Login</f7-login-screen-title>
            <f7-list form>
              <f7-list-item>
                <f7-label>Username</f7-label>
                <f7-input name="username" placeholder="Username" type="text"></f7-input>
              </f7-list-item>
              <f7-list-item>
                <f7-label>Password</f7-label>
                <f7-input name="password" type="password" placeholder="Password"></f7-input>
              </f7-list-item>
            </f7-list>
            <f7-list>
              <f7-list-button title="Sign In" close-login-screen></f7-list-button>
              <f7-list-label>
                <p>Click Sign In to close Login Screen</p>
              </f7-list-label>
            </f7-list>
          </f7-page>
        </f7-pages>
      </f7-view>
    </f7-login-screen>

  </div>
</template>

<script>
export default {
  data() {
    return {
      lists: [
        [
          {
            title: 'Accordion',
            link: '/accordion/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Autocomplete',
            link: '/autocomplete/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Calendar/Datepicker',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Cards',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Chips/Tags',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Contacts List',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Data Tables',
            link: '#',
            badge: 'NEW',
            badgeColor: 'green'
          }, {
            title: 'Floating Action Button',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Forms',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Grids',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Icons',
            link: '#',
            badge: '258',
            badgeColor: 'green'
          }, {
            title: 'Infinite Scroll',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Lazy Load Images',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'List View',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Login Screen',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Media Lists',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Messages',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Modals',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Navbars And Toolbars',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Notifications',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Photo Browser',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Picker',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Popover',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Preloader',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Progress Bar',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Pull To Refresh',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Search Bar',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Side Panels',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Sortable List',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Swipe To Delete',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Swiper Slider',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Tabs',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Timeline',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Virtual List',
            link: '#',
            badge: '',
            badgeColor: ''
          }
        ],
        [
          {
            title: 'Animation',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Color Themes',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Dynamically Generated Contend',
            link: '#',
            badge: '',
            badgeColor: ''
          }
        ],
        [
          {
            title: 'Transitions And Effects',
            link: '#',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Core Features',
            link: '#',
            badge: '',
            badgeColor: ''
          }
        ]
      ]
    }
  }
}
</script>

<style lang="less">
  html.ios-gt-8 .navbar .center{
    font-weight: 500;
  }
</style>
