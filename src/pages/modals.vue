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

    <!-- picker -->
    <f7-picker-modal>
      <f7-toolbar>
        <div class="left"></div>
        <div class="right">
          <f7-link close-picker>Done</f7-link>
        </div>
      </f7-toolbar>
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
