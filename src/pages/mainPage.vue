<template>
  <f7-page name="main">
    <f7-navbar>
      <f7-nav-center sliding>Framework7</f7-nav-center>
      <f7-nav-right>
        <f7-link icon="icon-bars" open-panel="right"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block-title>Welcome to Framework7</f7-block-title>
    <f7-block>
      <f7-button href="/about/">About Framework7</f7-button>
    </f7-block>
    <f7-block-title>FRAMEWORK7 KITCHEN SINK</f7-block-title>
    <f7-list v-for="list in lists" :key="list.id">
      <f7-list-item v-for="(item, index) in list.items"
        link-ignore-cache
        media="<i class='icon icon-f7'></i>"
        :link="item.link"
        :title="item.title"
        :class="item.class"
        :badge="item.badge"
        :badge-color="item.badgeColor"
        :key="index"
      ></f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      lists: [
        {
          id: 'items1',
          items: [
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
              link: '/notifications/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Photo Browser',
              link: '/photoBrowser/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Picker',
              link: '/picker/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Popover',
              link: '/popover/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Preloader',
              link: '/preloader/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Progress Bar',
              link: '/progressBar/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Pull To Refresh',
              link: '/pullToRefresh/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Search Bar',
              link: '/searchBar/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Side Panels',
              link: '/sidePanels/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Sortable List',
              link: '/sortableList/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Swipe To Delete',
              link: '/swipeToDelete/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Swiper Slider',
              link: '/swiperSlider/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Tabs',
              link: '/tabs/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Timeline',
              link: '/timeline/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Virtual List',
              link: '/virtualList/',
              badge: '',
              badgeColor: ''
            }
          ]
        }, {
          id: 'items2',
          items: [
            {
              title: 'Animation',
              link: '/animation/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Color Themes',
              link: '/colorThemes/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Dynamically Generated Contend',
              link: '#',
              class: 'ks-generate-page',
              badge: '',
              badgeColor: ''
            }
          ]
        }, {
          id: 'items3',
          items: [
            {
              title: 'Transitions And Effects',
              link: '/transitions/',
              badge: '',
              badgeColor: ''
            }, {
              title: 'Core Features',
              link: '/coreFeatures/',
              badge: '',
              badgeColor: ''
            }
          ]
        }
      ]
    }
  },
  mounted () {
    var dynamicPageIndex = 0
    var self = this

    function createContentPage() {
      self.$router.loadContent(
        '<!-- Top Navbar-->' +
        '<div class="navbar">' +
        '  <div class="navbar-inner">' +
        '    <div class="left sliding"><a href="#" class="back link"><i class="icon icon-back"></i><span>Back</span></a></div>' +
        '    <div class="center sliding">Dynamic Page ' + (++dynamicPageIndex) + '</div>' +
        '  </div>' +
        '</div>' +
        '<div class="pages">' +
        '  <!-- Page, data-page contains page name-->' +
        '  <div data-page="dynamic-content" class="page">' +
        '    <!-- Scrollable page content-->' +
        '    <div class="page-content">' +
        '      <div class="content-block">' +
        '        <div class="content-block-inner">' +
        '          <p>Here is a dynamic page created on ' + new Date() + ' !</p>' +
        '          <p>Go <a href="#" class="back">back</a> or generate <a href="#" class="ks-generate-page">one more page</a>.</p>' +
        '        </div>' +
        '      </div>' +
        '    </div>' +
        '  </div>' +
        '</div>'
      )
      return
    }

    this.$$(document).on('click', '.ks-generate-page', createContentPage)
  }
}
</script>