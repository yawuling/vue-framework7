<template>
  <f7-page>
    <f7-navbar title="Media Lists" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>Media Lists are almost the same as Data Lists, but with a more flexible layout for visualization of more complex data, like products, services, userc, etc. You can even use them in <f7-link open-popover>popovers</f7-link></f7-block>
    <f7-block-title>SONGS</f7-block-title>
    <f7-list media-list>
      <f7-list-item v-for="(item, index) in songs"
        :link="item.link"
        :media="item.media"
        :title="item.title"
        :subtitle="item.subtitle"
        :text="item.text"
        :after="item.after"
        :key="index"
      ></f7-list-item>
    </f7-list>
    <f7-block-title>Mail App (With Swipe to delete and overswipes)</f7-block-title>
    <f7-list media-list>
      <f7-list-item v-for="(item, index) in swipes"
        swipeout
        :link="item.link"
        :title="item.title"
        :subtitle="item.subtitle"
        :text="item.text"
        :after="item.after"
        :key="index">
        <f7-swipeout-actions left>
          <f7-swipeout-button reply color="green">Reply</f7-swipeout-button>
          <f7-swipeout-button forward color="blue">Forward</f7-swipeout-button>
        </f7-swipeout-actions>
        <f7-swipeout-actions right>
          <f7-swipeout-button more>More</f7-swipeout-button>
          <f7-swipeout-button mark color="orange">Mark</f7-swipeout-button>
          <f7-swipeout-button delete color="red">delete</f7-swipeout-button>
        </f7-swipeout-actions>
      </f7-list-item>
    </f7-list>
    <f7-block>SOMETHING MORE SIMPLE</f7-block>
    <f7-list media-list>
      <f7-list-item v-for="(item, index) in simples"
        :link="item.link"
        :media="item.media"
        :title="item.title"
        :subtitle="item.subtitle"
        :key="index"
      ></f7-list-item>
    </f7-list>
    <f7-block-title>INSET</f7-block-title>
    <f7-list media-list inset>
      <f7-list-item v-for="(item, index) in insets"
        :link="item.link"
        :media="item.media"
        :title="item.title"
        :subtitle="item.subtitle"
        :key="index"
      ></f7-list-item>
    </f7-list>

    <f7-popover>
      <f7-list media-list>
        <f7-list-item v-for="(item, index) in popovers"
          :link="item.link"
          :media="item.media"
          :title="item.title"
          :subtitle="item.subtitle"
          :key="index"
        ></f7-list-item>
      </f7-list>
    </f7-popover>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      songs: [
        {
          link: '#',
          media: '<img src="./static/image/photo1.jpg" width="80"/>',
          title: 'Yellow Submarine',
          subtitle: 'Beatles',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '$15'
        }, {
          link: '#',
          media: '<img src="./static/image/photo11.jpg" width="80" />',
          title: 'Don\'t Stop Me Now',
          subtitle: 'Queen',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '$22'
        }, {
          link: '#',
          media: '<img src="./static/image/photo6.jpg" width="80" />',
          title: 'Billie Jean',
          subtitle: 'Michael Jackson',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '$16'
        }
      ],
      swipes: [
        {
          link: '#',
          title: 'Facebook',
          subtitle: 'New messages from John Doe',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '17:14'
        }, {
          link: '#',
          title: 'John Doe(via Twitter)',
          subtitle: 'John Doe (@_johndoe) mentioned you on Twitter!',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '17:11'
        }, {
          link: '#',
          title: 'Facebook',
          subtitle: 'New messages from John Doe',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '16:48'
        }, {
          link: '#',
          title: 'John Doe(via Twitter)',
          subtitle: 'John Doe (@_johndoe) mentioned you on Twitter!',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '15:32'
        }
      ],
      simples: [
        {
          link: '',
          media: '<img src="./static/image/photo8.jpg" width="44"/>',
          title: 'Yellow Submarie',
          subtitle: 'Beatles',
        }, {
          link: '#',
          media: '<img src="./static/image/photo9.jpg" width="44"/>',
          title: 'Don\'t Stop Me Now',
          subtitle: 'Queen',
        }, {
          link: '',
          media: '<img src="./static/image/photo10.jpg" width="44"/>',
          title: 'Billie Jean',
          subtitle: 'Michael Jackson',
        }
      ],
      insets: [
        {
          link: '#',
          media: '<img src="./static/image/photo2.jpg" width="44"/>',
          title: 'Yellow Submarie',
          subtitle: 'Beatles',
        }, {
          link: '#',
          media: '<img src="./static/image/photo3.jpg" width="44"/>',
          title: 'Don\'t Stop Me Now',
          subtitle: 'Queen',
        }, {
          link: '#',
          media: '<img src="./static/image/photo4.jpg" width="44"/>',
          title: 'Billie Jean',
          subtitle: 'Michael Jackson',
        }
      ],
      popovers: [
        {
          link: '#',
          media: '<img src="./static/image/photo1.jpg" width="44"/>',
          title: 'Yellow Submarine',
          subtitle: 'Beatles',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '$15'
        }, {
          link: '#',
          media: '<img src="./static/image/photo11.jpg" width="44" />',
          title: 'Don\'t Stop Me Now',
          subtitle: 'Queen',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '$22'
        }, {
          link: '#',
          media: '<img src="./static/image/photo6.jpg" width="44" />',
          title: 'Billie Jean',
          subtitle: 'Michael Jackson',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sagittis tellus ut turpis condimentum, ut dignissim lacus tincidunt. Cras dolor metus, ultrices condimentum sodales sit amet, pharetra sodales eros. Phasellus vel felis tellus. Mauris rutrum ligula nec dapibus feugiat. In vel dui laoreet, commodo augue id, pulvinar lacus.',
          after: '$16'
        }
      ]
    }
  }
}
</script>

<style lang="less" scoped>
.popover{
  width: 240px;
}
</style>
