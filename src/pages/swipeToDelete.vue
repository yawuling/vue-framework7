<template>
  <f7-page>
    <f7-navbar title="Swipe To Delete" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        Swipe out actions on list elements is one of the most awesome F7 features. It allows you to call hidden menu for each list element where you can put default ready-to use delete button or any other buttons for some required actions.
      </p>
    </f7-block>
    <f7-block-title>SWIPE TO DELETE WITH CONFIRM MODAL</f7-block-title>
    <f7-list>
      <f7-list-item v-for="(item, index) in items1"
        media="<i class='icon icon-f7'></i>"
        :swipeout="item.isSwipeout"
        :title="item.title"
        :key="index">
        <f7-swipeout-actions>
          <f7-swipeout-button delete data-confirm="Are you sure you want to delete this item?">Delete</f7-swipeout-button>
        </f7-swipeout-actions>  
      </f7-list-item>
    </f7-list>
    <f7-block-title>SWIPE TO DELETE WITHOUT CONFIRM</f7-block-title>
    <f7-list>
      <f7-list-item v-for="(item, index) in items1"
        :swipeout="item.isSwipeout"
        :title="item.title"
        :key="index">
        <f7-swipeout-actions>
          <f7-swipeout-button delete>Delete</f7-swipeout-button>
        </f7-swipeout-actions>
      </f7-list-item>
    </f7-list>
    <f7-block-title>SWIPE FOR ACTIONS</f7-block-title>
    <f7-list>
      <f7-list-item v-for="(item, index) in items2"
        swipeout
        media="<i class='icon icon-f7'></i>"
        :title="item.title"
        :key="index">
        <f7-swipeout-actions>
          <f7-swipeout-button @click="onActions">More</f7-swipeout-button>
          <f7-swipeout-button delete v-if="item.isDelete">Delete</f7-swipeout-button>
        </f7-swipeout-actions>
      </f7-list-item>
    </f7-list>
    <f7-block-title>WITH CALLBACK ON REMOVE</f7-block-title>
    <f7-list>
      <f7-list-item v-for="(item, index) in items1"
        :swipeout="item.isSwipeout"
        @swipeout:deleted="onSwipeoutDeleted"
        :title="item.title"
        :key="index">
        <f7-swipeout-actions>
          <f7-swipeout-button delete>Delete</f7-swipeout-button>
        </f7-swipeout-actions>
      </f7-list-item>
    </f7-list>
    <f7-block-title>WITH ACTIONS ON LEFT SIDE (SWIPE TO RIGHT)</f7-block-title>
    <f7-list>
      <f7-list-item v-for="(item, index) in items3"
        swipeout
        media="<i class='icon icon-f7'></i>"
        :title="item.title"
        :key="index">
        <f7-swipeout-actions left>
          <f7-swipeout-button color="green" @click="onReply">Reply</f7-swipeout-button>
          <f7-swipeout-button color="blue" @click="onForward">Forward</f7-swipeout-button>
        </f7-swipeout-actions>
      </f7-list-item>
    </f7-list>
    <f7-block-title>ON BOTH SIDES WITH OVERSWIPES</f7-block-title>
    <f7-list media-list>
      <f7-list-item v-for="(item, index) in items4"
        swipeout
        :title="item.title"
        :subtitle="item.subtitle"
        :text="item.text"
        :after="item.after"
        :key="index">
        <f7-swipeout-actions left>
          <f7-swipeout-button color="green" @click="onReply">Reply</f7-swipeout-button>
          <f7-swipeout-button color="blue" @click="onForward">Forward</f7-swipeout-button>
        </f7-swipeout-actions>
        <f7-swipeout-actions right>
          <f7-swipeout-button @click="onActions">More</f7-swipeout-button>
          <f7-swipeout-button color="orange" @click="onMark">Mark</f7-swipeout-button>
          <f7-swipeout-button delete>Delete</f7-swipeout-button>
        </f7-swipeout-actions>
      </f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      items1: [
        {
          title: 'Swipe left on me please',
          isSwipeout: true
        }, {
          title: 'Swipe left on me too',
          isSwipeout: true
        }, {
          title: 'I am not removeable',
          isSwipeout: false
        }
      ],
      items2: [
        {
          title: 'Swipe left on me please',
          isDelete: true
        }, {
          title: 'Swipe left on me too',
          isDelete: true
        }, {
          title: 'You can\'n delete me',
          isDelete: false
        }
      ],
      items3: [
        {
          title: 'Swipe right on me please'
        }, {
          title: 'Swipe right on me too'
        }
      ],
      items4: [
        {
          title: 'Facebook',
          subtitle: 'New messages from John Doe',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '17:14'
        }, {
          title: 'John Doe (via Twitter)',
          subtitle: 'John Doe (@_johndoe) mentioned you on Twitter!',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '17:11'
        }, {
          title: 'Facebook',
          subtitle: 'New messages from John Doe',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '17:14'
        }, {
          title: 'John Doe (via Twitter)',
          subtitle: 'John Doe (@_johndoe) mentioned you on Twitter!',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '17:11'
        }
      ]
    }
  },
  methods: {
    onActions: function () {
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
      this.$f7.actions([buttons1, buttons2])
    },
    onSwipeoutDeleted: function () {
      this.$f7.alert('Thanks, item removed!')
    },
    onReply: function () {
      this.$f7.alert('Reply')
    },
    onForward: function () {
      this.$f7.alert('Forward')
    },
    onMark: function () {
      this.$f7.alert('Mark')
    }
  }
}
</script>

<style lang="less">

</style>
