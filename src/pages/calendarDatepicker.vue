<template>
  <f7-page>
    <f7-navbar title="Calendar" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        Calendar is a touch optimized component that provides an easy way to handle dates.
      </p>
      <p>
        Calendar could be used as inline component or as overlay. Overlay Calendar will be automatically converted to Popover on tablets (iPad).
      </p>
    </f7-block>
    <f7-block-title>DEFAULT SETUP</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Your birth date" readonly id="calendar-default"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>CUSTOM DATE FORMAT</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Select date" readonly id="calendar-date-format"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>MULTIPLE VALUES</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Select multiple dates" readonly id="calendar-multiple"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>RANGE PICKER <f7-badge color="green">NEW</f7-badge></f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Select date range" readonly id="calendar-range"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>WITH EVENTS</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Select date" readonly id="calendar-events"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>DISABLED DATES</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Select date" readonly id="calendar-disabled"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block>
      <div class="content-block-inner">
        <div id="calendar-inline-container"></div>
      </div>
    </f7-block>
  </f7-page>
</template>

<<script>
export default {
  mounted () {
    let calendarDefault = this.$f7.calendar({
      input: '#calendar-default'
    })
    let calendarDateFormat = this.$f7.calendar({
      input: '#calendar-date-format',
      dateFormat: 'DD, MM dd, yyyy'
    })
    let calendarMultiple = this.$f7.calendar({
      input: '#calendar-multiple',
      dateFormat: 'M dd yyyy',
      multiple: true
    })
    let calendarRange = this.$f7.calendar({
      input: '#calendar-range',
      dateFormat: 'M dd yyyy',
      rangePicker: true
    })
    let today = new Date()
    let weekLater = new Date().setDate(today.getDate() + 7)
    let calendarEvents = this.$f7.calendar({
      input: '#calendar-events',
      dateFormat: 'M dd yyyy',
      events: {
        from: today,
        to: weekLater
      }
    })
    let calendarDisabled = this.$f7.calendar({
      input: '#calendar-disabled',
      dateFormat: 'M dd yyyy',
      disabled: {
        from: today,
        to: weekLater
      }
    })

    let monthNames = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'Augest', 'September', 'October', 'November', 'December'];

    let calendarInline = this.$f7.calendar({
      container: '#calendar-inline-container',
      value: [new Date()],
      weekHeader: false,
      toolbarTemplate:
        '<div class="toolbar calendar-custom-toolbar">' +
          '<div class="toolbar-inner">' +
            '<div class="left">' +
              '<a href="#" class="link icon-only"><i class="icon icon-back"></i></a>' +
            '</div>' +
            '<div class="center"></div>' +
            '<div class="right">' +
              '<a href="" class="link icon-only"><i class="icon icon-forward"></i></a>' +
            '</div>' +
          '</div>' +
        '</div>',
      onOpen: (p) => {
        window.Dom7('.calendar-custom-toolbar .center').text(monthNames[p.currentMonth] + ', ' + p.currentYear)
        window.Dom7('.calendar-custom-toolbar .left .link').on('click', () => {
          calendarInline.prevMonth()
        })
        window.Dom7('.calendar-custom-toolbar .right .link').on('click', () => {
          calendarInline.nextMonth()
        })
      },
      onMonthYearChangeStart: (p) => {
        window.Dom7('.calendar-custom-toolbar .center').text(monthNames[p.currentMonth] + ', ' + p.currentYear)
      }
    })
  }
}
</script>

<style lang="less" scoped>
.content-block{

  .content-block-inner{
    padding-top: 0;
  }
}
</style>
