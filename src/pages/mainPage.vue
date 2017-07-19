<template>
  <f7-page>
    <f7-navbar>
      <f7-nav-center sliding>Framework7</f7-nav-center>
      <f7-nav-right>
        <f7-link icon="icon-bars" open-panel="right"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <!-- Material Theme Toolbar -->
    <f7-toolbar v-if="$theme.material">
      <f7-link>Dummy Link</f7-link>
      <f7-link>Menu</f7-link>
    </f7-toolbar>
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
</template>

<script>
export default {
  data () {
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
            title: 'Calendar / Datepicker',
            link: '/calendarDatepicker/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Cards',
            link: '/cards/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Chips/Tags',
            link: '/chipsTags/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Contacts List',
            link: '/contacts/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Floating Action Button',
            link: '/floatingAction/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Forms',
            link: '/forms/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Grid',
            link: '/grid/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Icons',
            link: '/icons/',
            badge: '258',
            badgeColor: 'green'
          }, {
            title: 'Infinite Scroll',
            link: '/infiniteScroll/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Lazy Load Images',
            link: '/lazyLoadImages/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'List View',
            link: '/listView/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Login Screen',
            link: '/loginScreen/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Media Lists',
            link: '/mediaLists/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Messages',
            link: '/messages/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Modals',
            link: '/modals/',
            badge: '',
            badgeColor: ''
          }, {
            title: 'Navbars And Toolbars',
            link: '/navbarsAndToolbars/',
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