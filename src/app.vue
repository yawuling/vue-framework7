<template>
  <!-- App -->
  <div id="app">

    <!-- Statusbar -->
    <f7-statusbar></f7-statusbar>

    <!-- Left Panel -->
    <f7-panel left cover layout="dark">
      <f7-view id="left-panel-view">
        <f7-pages>
          <f7-page>
            <f7-block-title>LEFT PANEL</f7-block-title>
            <f7-block>
              <p>
                This is a side panel. You can close it by clicking outsite or on this link: <f7-link close-panel="left">close me</f7-link>. You can put here anything, even another isolated view like in <f7-link open-panel="right">Right Panel</f7-link>
              </p>
            </f7-block>
            <f7-block-title>FRAMEWORK7 KITCHEN SINK</f7-block-title>
            <f7-list>
              <f7-list-item v-for="(item, index) in items"
                  media="<i class='icon icon-f7'></i>"
                  link-close-panel
                  link-view=".view-main"
                  :link="item.link"
                  :title="item.title"
                  :key="index"
              ></f7-list-item>
            </f7-list>
            <f7-block>
              <p>
                Long text block goes here. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras sem urna, gravida non scelerisque id, fringilla ac velit. Phasellus elementum a ipsum at ornare. Mauris sagittis rhoncus euismod. Integer convallis augue eu lacus ultrices, in dictum elit consequat. Nulla faucibus massa id felis egestas eleifend. Proin consequat dignissim magna ut scelerisque. Vestibulum ac lorem semper, posuere sapien nec, pharetra massa. Nulla a tellus facilisis, sollicitudin quam porta, aliquam lorem. Fusce dignissim eros ac diam molestie, ut ultrices lorem tristique. Ut facilisis augue ac nisi egestas malesuada. Nunc posuere tortor quis eleifend mollis. Aliquam erat volutpat. Donec feugiat elit tellus, nec convallis orci elementum in. Sed urna mi, vestibulum id tempus id, pretium et ante. Pellentesque eget sollicitudin ligula. Phasellus pellentesque velit eu porta suscipit.
              </p>
            </f7-block>
          </f7-page>
        </f7-pages>
      </f7-view>
    </f7-panel>

    <!-- Right Panel -->
    <f7-panel right reveal layout="dark">
      <f7-view id="right-panel-view" navbar-through :dynamic-navbar="true">
        <f7-navbar v-if="$theme.ios" title="Right Panel" sliding></f7-navbar>
        <f7-pages>
          <f7-page>
            <f7-navbar v-if="$theme.material" title="Right Panel" sliding></f7-navbar>
            <f7-block>
              <p>
                This is a right side panel. You can close it by clicking outsite or on this link: <f7-link close-panel>close me</f7-link>. You can put here anything, even another isolated view, try it:
              </p>
            </f7-block>
            <f7-list>
              <f7-list-item
                title="Right panel page 2"
                link="/sidePanels/panelRight2/"
              ></f7-list-item>
              <f7-list-item
                title="Right panel page 3"
                link="/sidePanels/panelRight3/"
              ></f7-list-item>
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
          <f7-link open-popover>Menu</f7-link>
        </f7-toolbar>
      </f7-view>
    </f7-views>

    <!-- popup -->
    <f7-popup tablet-fullscreen>
      <f7-view navbar-fixed>
        <f7-pages>
          <f7-page>
            <f7-navbar title="Popup Title">
              <f7-nav-right>
                <f7-link close-popup>Done</f7-link>
              </f7-nav-right>
            </f7-navbar>
            <f7-block>
              <p>
                Here comes popup. You can put here anything, even independent view with its own navigation. Also not, that by default popup looks a bit different on iPhone/iPod and iPad, on iPhone it is fullscreen.
              </p>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse faucibus mauris leo, eu bibendum neque congue non. Ut leo mauris, eleifend eu commodo a, egestas ac urna. Maecenas in lacus faucibus, viverra ipsum pulvinar, molestie arcu. Etiam lacinia venenatis dignissim. Suspendisse non nisl semper tellus malesuada suscipit eu et eros. Nulla eu enim quis quam elementum vulputate. Mauris ornare consequat nunc viverra pellentesque. Aenean semper eu massa sit amet aliquam. Integer et neque sed libero mollis elementum at vitae ligula. Vestibulum pharetra sed libero sed porttitor. Suspendisse a faucibus lectus.
              </p>
              <p>
                Duis ut mauris sollicitudin, venenatis nisi sed, luctus ligula. Phasellus blandit nisl ut lorem semper pharetra. Nullam tortor nibh, suscipit in consequat vel, feugiat sed quam. Nam risus libero, auctor vel tristique ac, malesuada ut ante. Sed molestie, est in eleifend sagittis, leo tortor ullamcorper erat, at vulputate eros sapien nec libero. Mauris dapibus laoreet nibh quis bibendum. Fusce dolor sem, suscipit in iaculis id, pharetra at urna. Pellentesque tempor congue massa quis faucibus. Vestibulum nunc eros, convallis blandit dui sit amet, gravida adipiscing libero.
              </p>
              <p>
                Morbi posuere ipsum nisl, accumsan tincidunt nibh lobortis sit amet. Proin felis lorem, dictum vel nulla quis, lobortis dignissim nunc. Pellentesque dapibus urna ut imperdiet mattis. Proin purus diam, accumsan ut mollis ac, vulputate nec metus. Etiam at risus neque. Fusce tincidunt, risus in faucibus lobortis, diam mi blandit nunc, quis molestie dolor tellus ac enim. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse interdum turpis a velit vestibulum pharetra. Vivamus blandit dapibus cursus. Aenean lorem augue, vehicula in eleifend ut, imperdiet quis felis.
              </p>
              <p>
                Duis non erat vel lacus consectetur ultricies. Sed non velit dolor. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Proin vel varius mi, a tristique ante. Vivamus eget nibh ac elit tempor bibendum sit amet vitae velit. Proin sit amet dapibus nunc, non porta tellus. Fusce interdum vulputate imperdiet. Sed faucibus metus at pharetra fringilla. Fusce mattis orci et massa congue, eget dapibus ante rhoncus. Morbi semper sed tellus vel dignissim. Cras vestibulum, sapien in suscipit tincidunt, lectus mi sodales purus, at egestas ligula dui vel erat. Etiam cursus neque eu lectus eleifend accumsan vitae non leo. Aliquam scelerisque nisl sed lacus suscipit, ac consectetur sapien volutpat. Etiam nulla diam, accumsan ut enim vel, hendrerit venenatis sem. Vestibulum convallis justo vitae pharetra consequat. Mauris sollicitudin ac quam non congue.
              </p>
            </f7-block>
          </f7-page>
        </f7-pages>
      </f7-view>
    </f7-popup>

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

    <f7-popover style="width: 240px">
      <f7-list>
        <f7-list-button v-for="(btn, index) in popoverBtns" 
          :href="btn.link"
          :key="index"
          close-popover
        >{{btn.title}}</f7-list-button>
      </f7-list>
    </f7-popover>
  </div>
</template>

<script>
import MainPage from './pages/mainPage.vue'

export default {
  data () {
    return {
      username: '',
      password: '',
      items: [
        {
          title: 'Forms',
          link: '/forms/'
        }, {
          title: 'List View',
          link: '/listView/'
        }, {
          title: 'Media Lists',
          link: '/mediaLists/'
        }, {
          title: 'Modals',
          link: '/modals/'
        }, {
          title: 'Navbars And Toolbars',
          link: '/navbarsAndToolbars/'
        }, {
          title: 'Popover',
          link: '/popover/'
        }, {
          title: 'Side Panels',
          link: '/sidePanels/'
        }, {
          title: 'Swipe To Delete',
          link: '/swipeToDelete/',
        }, {
          title: 'Swiper Slider',
          link: '/swiperSlider/',          
        }, {
          title: 'Tabs',
          link: '/tabs/'
        }
      ],
      popoverBtns: [
        {
          title: 'Modals',
          link: '/modals/'
        }, {
          title: 'Popover',
          link: '/popover/'
        }, {
          title: 'Tabs',
          link: '/tabs/'
        }, {
          title: 'Side Panels',
          link: '/sidePanels/'
        }, {
          title: 'List View',
          link: '/listView/'
        }, {
          title: 'Forms',
          link: '/forms/'
        }
      ]
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
