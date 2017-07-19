<template>
  <f7-page>
    <f7-navbar title="Modals" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block inner>
      <p>There are 1:1 replacements of native Alert, Prompt and Confirm modals. They support callbacks, have very easy api and can be combined with each other. Check these examples:</p>
      <f7-grid class="modals-grid">
        <f7-col width="33">
          <f7-button @click="doAlert">Alert</f7-button>
        </f7-col>
        <f7-col width="33">
          <f7-button @click="doConfirm">Confirm</f7-button>
        </f7-col>
        <f7-col width="33">
          <f7-button @click="doPrompt">Prompt</f7-button>
        </f7-col>
      </f7-grid>
      <f7-grid class="modals-grid">
        <f7-col width="50">
          <f7-button @click="doLogin">Login Modal</f7-button>
        </f7-col>
        <f7-col width="50">
          <f7-button @click="doPassword">Password Modal</f7-button>
        </f7-col>
      </f7-grid>
      <f7-grid class="modals-grid">
        <f7-col width="50">
          <f7-button @click="doAction">Action Sheet</f7-button>
        </f7-col>
        <f7-col width="50">
          <f7-button open-popup>Popup</f7-button>
        </f7-col>
      </f7-grid>
    </f7-block>
    <f7-block-title>ACTION SHEET TO POPOVER</f7-block-title>
    <f7-block inner>
      <p>
        Action Sheet could be automatically converted to Popover (for tablets). This button will open Popover on tablets and Action Sheet on phones:
        <f7-button style="display: inline-block;vertical-align: center;" @click="doAction">Action/Popover</f7-button>
      </p>
    </f7-block>
    <f7-block-title>PICKER MODAL</f7-block-title>
    <f7-block inner>
      <p>
        Such overlay type is similar to <f7-link>Picker's</f7-link> overlay, but also allows to create custom picker overlays
      </p>
      <p>
        <f7-button open-picker>Picker Modal With Custom HTML</f7-button>
      </p>
    </f7-block>
    <f7-block-title>MODALS STACK</f7-block-title>
    <f7-block inner>
      <p>
        This feature doesn't allow to open multiple modals at the same time, and will automatically open next modal when you close the current one. Such behavior is similar to browser native alerts:
      </p>
      <p>
        <f7-button @click="doMulAlerts">Open Multiple Alerts</f7-button>
      </p>
    </f7-block>

    <!-- popup -->
    <f7-popup>
      <f7-page navbar-fixed>
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
    </f7-popup>

    <!-- picker -->
    <f7-picker-modal>
      <f7-navbar>
        <f7-nav-right>
          <f7-link close-picker>Done</f7-link>
        </f7-nav-right>
      </f7-navbar>
      <f7-block>
        Integer mollis nulla id nibh elementum finibus. Maecenas eget fermentum ipsum. Sed sagittis condimentum nisl at tempus. Duis lacus libero, laoreet vitae ligula a, aliquet eleifend sapien. Nullam sodales viverra sodales. Nulla hendrerit condimentum dolor facilisis tempor. Donec at est malesuada, sagittis nisi et, accumsan enim.
      </f7-block>
    </f7-picker-modal>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      alert: false
    }
  },
  methods: {
    doAlert: function () {
      this.$f7.alert('Hello')
    },
    doConfirm: function () {
      let f7 = this.$f7

      f7.confirm('Are you feel good today?', function () {
        f7.alert('Great!', 'Framework7')
      })
    },
    doPrompt: function () {
      let f7 = this.$f7

      f7.prompt('What is your name?', function (value) {
        f7.confirm('Are you sure your name is ' + value + '?', function () {
          f7.alert('Your name is ' + value + ' :)')
        })
      })
    },
    doLogin: function () {
      let f7 = this.$f7

      f7.modalLogin('Enter your username and password', function (username, password) {
        f7.alert('Thank you! Username: ' + username + ', password: ' + password)
      })
    },
    doPassword: function () {
      let f7 = this.$f7

      f7.modalPassword('Enter your password', function (password) {
        f7.alert('Thank you! Password: ' + password)
      })
    },
    doAction: function () {
      let f7 = this.$f7

      let buttons1 = [
        {
          text: 'Here comes some optional description or warming for actions below',
          label: true
        }, {
          text: 'Alert',
          onClick: function () {
            f7.alert('He Hoou!')
          }
        }, {
          text: 'Nice Red Button',
          color: 'red',
          onClick: function () {
            f7.alert('You have clicked red button!')
          }
        }
      ]
      let buttons2 = [
        {
          text: 'Cancel',
          bold: true
        }
      ]
      let group = [buttons1, buttons2]

      f7.actions(group)
    },
    doMulAlerts: function () {
      let f7 = this.$f7

      f7.alert('Alert 1', function () {
        f7.alert('Alert 2', function () {
          f7.alert('Alert 3', function () {
            f7.alert('Alert 4', function () {
              f7.alert('Alert 5')
            })
          })
        })
      })
    }
  }
}
</script>

<style lang="less" scoped>
.modals-grid{
  margin: 1em 0;
}
</style>
