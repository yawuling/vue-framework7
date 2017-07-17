<template>
  <f7-page>
    <f7-navbar title="Contacts" back-link="返回" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-list contacts>
      <f7-list-group v-for="(group, key) in contacts">
        <f7-list-item :title="key" group-title></f7-list-item>
        <f7-list-item v-for="name in group" :title="name"></f7-list-item>
      </f7-list-group>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      contacts: {
        'A': [
          'Aaron',
          'Abbie',
          'Adam',
          'Adele',
          'Agatha',
          'Agnes',
          'Albert',
          'Alexander'
        ],
        'B': [
          'Bailey',
          'Barclay',
          'Bartolo',
          'Bellamy',
          'Belle',
          'Benjamin'
        ],
        'C': [
          'Caiden',
          'Calvin',
          'Candy',
          'Carl',
          'Cherilyn',
          'Chester',
          'Chloe'
        ],
        'V': [
          'Vladimir'
        ]
      }
    }
  }
}
</script>

<style lang="less">
</style>
