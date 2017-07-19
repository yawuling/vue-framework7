<template>
  <f7-page>
    <f7-navbar title="Smart Selects" back-link="Forms" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>Framework7 allows you to easily convert your usual form selects to dynamic pages with radios:</f7-block>
    <f7-list form>
      <f7-list-item smart-select title="Fruit" smart-select-back-text="Back">
        <select name="fruits">
          <option value="apple" selected>Apple</option>
          <option value="pineapple">Pineapple</option>
          <option value="pear">Pear</option>
          <option value="orange">Orange</option>
          <option value="melon">Melon</option>
          <option value="peach">Peach</option>
          <option value="banana">Banana</option>
        </select>
      </f7-list-item>
      <f7-list-item smart-select title="Car" smart-select-back-text="Back">
        <select name="car" multiple="multiple">
          <optgroup label="Japanese">
            <option value="honda" selected>Honda</option>
            <option value="lexus">Lexus</option>
            <option value="mazda">Mazda</option>
            <option value="nissan">Nissan</option>
            <option value="toyota">Toyota</option>
          </optgroup>
          <optgroup label="German">
            <option value="audi" selected>Audi</option>
            <option value="bmw">BMW</option>
            <option value="mercedes">Mercedes</option>
            <option value="vw">Volkswagen</option>
            <option value="volvo">Volvo</option>
          </optgroup>
          <optgroup label="American">
            <option value="cadillac">Cadillac</option>
            <option value="chrysler">Chrysler</option>
            <option value="dodge">Dodge</option>
            <option value="ford" selected>Ford</option>
          </optgroup>
        </select>
      </f7-list-item>
      <f7-list-item smart-select smart-select-back-on-select title="Mac or Windows" smart-select-back-text="Back">
        <select name="mac-windows">
          <option value="mac">Mac</option>
          <option value="windows">Windows</option>
        </select>
      </f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  
}
</script>

<style lang="less">

</style>
