<template>
  <f7-page>
    <f7-navbar title="List View" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>Framework7 allows you to be flexible with list views (table views). You can make them as navigation menus, you can use there icons, inputs, and any elements inside of the list, and even make them nested:</f7-block>
    <f7-block-title>DATA LIST, WITH ICONS</f7-block-title>
    <f7-list>
      <f7-list-item
        media="<i class='icon icon-f7'></i>"
        title="Ivan Petrov"
        after="CEO"
      ></f7-list-item>
      <f7-list-item
        media="<i class='icon icon-f7'></i>"
        title="John Doe"
        badge="5"
        badge-color="gray"
      ></f7-list-item>
      <f7-list-item
        media="<i class='icon icon-f7'></i>"
        title="Jenna Smith"
      ></f7-list-item>
    </f7-list>
    <f7-block-title>LINKS</f7-block-title>
    <f7-list>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i>"
        title="Ivan Petrov"
        after="CEO"
      ></f7-list-item>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i>"
        title="John Doe"
        badge="5"
        badge-color="gray"
      ></f7-list-item>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i>"
        title="Jenna Smith"
      ></f7-list-item>
    </f7-list>
    <f7-block-title>LINKS, NO ICONS</f7-block-title>
    <f7-list>
      <f7-list-item
        link="#"
        title="Ivan Petrov"
        after="CEO"
      ></f7-list-item>
      <f7-list-item
        link="#"
        title="John Doe"
        badge="5"
        badge-color="gray"
      ></f7-list-item>
      <f7-list-item title="Divider Here" divider></f7-list-item>
      <f7-list-item
        link="#"
        title="Ivan Petrov"
        after="CEO"
      ></f7-list-item>
      <f7-list-item
        link="#"
        title="John Doe"
        badge="5"
        badge-color="gray"
      ></f7-list-item>
    </f7-list>
    <f7-block-title>GROUPED WITH STICKY TITLES</f7-block-title>
    <f7-list>
      <f7-list-group v-for="(group, key) in groups" :key="key">
        <f7-list-item :title="key" group-title></f7-list-item>
        <f7-list-item v-for="(item, index) in group" :title="item" :key="index"></f7-list-item>
      </f7-list-group>
    </f7-list>
    <f7-block-title>MIXED AND NESTED</f7-block-title>
    <f7-list>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i>"
        title="Ivan Petrov"
        after="CEO"
      ></f7-list-item>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i><i class='icon icon-f7'></i>"
        title="Two icons here"
      ></f7-list-item>
      <f7-list-item title="No icons here">
        <ul slot="root">
          <f7-list-item
            link="#"
            media="<i class='icon icon-f7'></i>"
            title="Ivan Petrov"
            after="CEO"
          ></f7-list-item>
          <f7-list-item
            link="#"
            media="<i class='icon icon-f7'></i><i class='icon icon-f7'></i>"
            title="Two icons here"
          ></f7-list-item>
          <f7-list-item title="No icons here"></f7-list-item>
          <f7-list-item
            link="#"
            media="<i class='icon icon-f7'></i>"
            title="Ultra long text goes here, no, it is really really long"
          ></f7-list-item>
          <f7-list-item
            media="<i class='icon icon-f7'></i>"
            title="With switch">
            <f7-input type='switch' slot="after"></f7-input>
          </f7-list-item>
        </ul>
      </f7-list-item>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i>"
        title="Ultra long text goes here, no, it is really really long"
      ></f7-list-item>
      <f7-list-item
        media="<i class='icon icon-f7'></i>"
        title="With switch">
        <f7-input type="switch" slot="after"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>MIXED, INSET</f7-block-title>
    <f7-list inset>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i>"
        title="Ivan Petrov"
        after="CEO"
      ></f7-list-item>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i><i class='icon icon-f7'></i>"
        title="Two icons here"
      ></f7-list-item>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i>"
        title="Ultra long text goes here, no, it is really really long"
      ></f7-list-item>
      <f7-list-item
        media="<i class='icon icon-f7'></i>"
        title="With switch">
        <f7-input type="switch" slot="after"></f7-input>
      </f7-list-item>
      <f7-list-label>
        <p>Here comes some useful information about list above</p>
      </f7-list-label>
    </f7-list>
    <f7-block-title>TABLET INSET</f7-block-title>
    <f7-list tablet-inset>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i>"
        title="Ivan Petrov"
        after="CEO"
      ></f7-list-item>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i><i class='icon icon-f7'></i>"
        title="Two icons here"
      ></f7-list-item>
      <f7-list-item
        link="#"
        media="<i class='icon icon-f7'></i>"
        title="Ultra long text goes here, no, it is really really long"
      ></f7-list-item>
      <f7-list-label>This list block will look like "inset" only on tablets (iPad)</f7-list-label>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      groups: {
        'A': [
          'Aaron',
          'Abble',
          'Adam'
        ],
        'B': [
          'Bailey',
          'Barclay',
          'Bartolo'
        ],
        'C': [
          'Calden',
          'Calvin',
          'Candy'
        ]
      }
    }
  }
}
</script>

<style lang="less">

</style>
