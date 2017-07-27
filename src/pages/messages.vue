<template>
  <f7-page no-toolbar toolbar-fixed>
    <f7-navbar title="Messages" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-messages>
      <f7-message v-for="(message, index) in messages"
        :text="message.text"
        :label="message.label"
        :date="message.date"
        :name="message.name"
        :avatar="message.avatar"
        :type="message.type"
        :day="message.day"
        :time="message.time"
        :key="index"
      >
        <img v-if="message.img" :src="message.img" />
      </f7-message>
    </f7-messages>
    <f7-messagebar placeholder="Message" send-link="Send" @submit="onSubmit" v-model="messageText">
      <f7-link slot="before-textarea" class="icon-only">
        <f7-icon icon="icon icon-camera"></f7-icon>
      </f7-link>
    </f7-messagebar>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      messages: [
        {
          day: 'Sunday, Feb 9, ',
          time: '12:58'
        }, {
          text: 'Hi, Kate'
        }, {
          text: 'How are you?'
        }, {
          name: 'Kate Johnson',
          avatar: './static/image/photo5.jpg',
          text: 'Hi, i am good',
          type: 'received'
        }, {
          name: 'Blue Ninja',
          avatar: './static/image/photo7.jpg',
          text: 'Hi there, I am also fine, thanks! And how are you?',
          type: 'received'
        }, {
          text: 'Hey, Blue Ninja! Glad to see you ;)'
        }, {
          text: 'What do you think about my new logo?'
        }, {
          day: 'Wednesday, Feb 12, ',
          time: '19:33'
        }, {
          text: 'Hey? Any thoughts about my new logo?'
        }, {
          day: 'Thursday, Feb 13, ',
          time: '11:20'
        }, {
          text: 'Alo...'
        }, {
          text: 'Are you there?'
        }, {
          name: 'Blue Ninja',
          avatar: './static/image/photo7.jpg',
          text: 'Hi, i am here',
          type: 'received'
        }, {
          name: 'Blue Ninja',
          avatar: './static/image/photo7.jpg',
          text: 'Your logo is great',
          type: 'received'
        }, {
          name: 'Kate Johnson',
          avatar: './static/image/photo5.jpg',
          text: 'Leave me alone',
          type: 'received'
        }, {
          text: ':('
        }, {
          text: 'Hey, look, cutest kitten ever!'
        }, {
          img: './static/image/animal1.jpg'
        }, {
          name: 'Blue Ninja',
          avatar: './static/image/photo7.jpg',
          text: 'Yep',
          type: 'received'
        }, {
          text: 'Cool',
          label: 'Delivered 1 week ago'
        }
      ],
      messageText: '',
      conversationStarted: false
    }
  },
  methods: {
    onSubmit: function () {
      let messages = this.$f7.messages('.messages'),
          messageBar = this.$f7.messagebar('.messagebar'),
          messageInfo = this.messageText.trim(),
          message

      if (messageInfo.length === 0) {
        return
      }

      if (!this.conversationStarted && this.messageText) {
        message = {
          day: 'Today',
          time: (new Date()).getHours() + ':' + (new Date()).getMinutes()
        }
        this.messages.push(message)
      }

      if (this.messageText) {
        message = {
          img: '',
          text: this.messageText
        }
        this.messages.push(message)
      }

      this.messageText = ''
      this.conversationStarted = true
      messageBar.clear()
    }
  }
}
</script>

<style lang="less" scoped>
.toolbar.messagebar{
  transform: none;
  transition: 0ms;
}
</style>
