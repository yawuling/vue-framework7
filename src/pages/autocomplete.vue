<template>
  <f7-page>
    <f7-navbar title="Autocomplete" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>DROPDOWN AUTOCOMPLETE</f7-block>
    <f7-block>Dropdown autocomplete is good to use as a quick and simple solution to provide more options in addition to free-type value.</f7-block>
    <f7-block-title>SIMPLE DROPDOWN AUTOCOMPLETE</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-label>Fruit</f7-label>
        <f7-input type="text" placeholder="Fruit" id="autocomplete-dropdown"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>DROPDOWN WITH INPUT EXPANDED</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-label>Fruit</f7-label>
        <f7-input type="text" placeholder="Fruit" id="autocomplete-dropdown-expand"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>DROPDOWN WITH ALL VALUES</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-label>Fruit</f7-label>
        <f7-input type="text" placeholder="Fruit" id="autocomplete-dropdown-all"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>DROPDOWN WITH PLACEHOLDER</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-label>Fruit</f7-label>
        <f7-input type="text" placeholder="Fruit" id="autocomplete-dropdown-placeholder"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>DROPDOWN WITH AJAX-DATA</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-label>Language</f7-label>
        <f7-input type="text" placeholder="Language" id="autocomplete-dropdown-ajax"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>SIMPLE STANDALONE AUTOCOMPLETE</f7-block-title>
    <f7-list form>
      <f7-list-item link="#" title="Favorite Fruit" :after="standaloneFruit" id="autocomplete-standalone">
        <input type="hidden" :value="standaloneFruit"/>
      </f7-list-item>
    </f7-list>
    <f7-block-title>POPUP STANDALONE AUTOCOMPLETE</f7-block-title>
    <f7-list form>
      <f7-list-item link="#" title="Favorite Fruit" :after="popupFruit" id="autocomplete-popup">
        <input type="hidden" :value="popupFruit"/>
      </f7-list-item>
    </f7-list>
    <f7-block-title>MULTIPLE VALUES STANDALONE AUTOCOMPLETE</f7-block-title>
    <f7-list form>
      <f7-list-item link="#" title="Favorite Fruit" :after="multiFruit" id="autocomplete-multiple">
        <input type="hidden" :value="multiFruit"/>
      </f7-list-item>
    </f7-list>
    <f7-block-title>STANDALONE WITH AJAX_DATA</f7-block-title>
    <f7-list form>
      <f7-list-item link="#" title="Language" :after="ajaxLanguageTitle" id="autocomplete-standalone-ajax">
        <input type="hidden" :value="ajaxLanguage"/>
      </f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      fruits: ('Apple Apricot Avocado Banana Melon Orange Peach Pear Pineapple').split(' '),
      standaloneFruit: '',
      popupFruit: '',
      multiFruit: '',
      ajaxLanguageTitle: '',
      ajaxLanguage: ''
    }
  },
  mounted() {
    let self = this;
    let fruits = self.fruits
    let autocompleteDropdownSimple = this.$f7.autocomplete({
      input: '#autocomplete-dropdown',
      openIn: 'dropdown',
      source: function (autocomplete, query, render) {
        let results = []
        if (query.length === 0) {
          render(results)
          return
        }
        for (let i = 0; i < fruits.length; i++) {
          if (fruits[i].toLowerCase().indexOf(query.toLowerCase()) >= 0) {
            results.push(fruits[i])
          }
        }
        render(results)
      }
    })
    let autocompleteDropdownExpand = this.$f7.autocomplete({
      input: '#autocomplete-dropdown-expand',
      openIn: 'dropdown',
      expandInput: true,
      source: function (autocomplete, query, render) {
        let results = [];
        if (query.length === 0) {
          render(results)
          return
        }
        for (let i = 0; i < fruits.length; i++) {
          if (fruits[i].toLowerCase().indexOf(query.toLowerCase()) >= 0) {
            results.push(fruits[i])
          }
        }
        render(results)
      }
    })
    let autocompleteDropdownAll = this.$f7.autocomplete({
      input: '#autocomplete-dropdown-all',
      openIn: 'dropdown',
      source: function (autocomplete, query, render) {
        let results = [];
        for (let i = 0; i < fruits.length; i++) {
          if (fruits[i].toLowerCase().indexOf(query.toLowerCase()) >= 0) {
            results.push(fruits[i]);
          }
        }
        render(results)
      }
    })
    let autocompleteDropdownPlaceholder = this.$f7.autocomplete({
      input: '#autocomplete-dropdown-placeholder',
      openIn: 'dropdown',
      dropdownPlaceholderText: 'Try to type "Apple"',
      source: function (autocomplete, query, render) {
        let results = []
        if (query.length === 0) {
          render(results)
          return
        }
        for (let i = 0; i < fruits.length; i++) {
          if (fruits[i].toLowerCase().indexOf(query.toLowerCase()) >= 0) {
            results.push(fruits[i])
          }
        }
        render(results)
      }
    })
    let autocompleteDropdownAjax = this.$f7.autocomplete({
      input: '#autocomplete-dropdown-ajax',
      openIn: 'dropdown',
      preloader: true,
      valueProperty: 'id',
      textProperty: 'name',
      limit: 20,
      dropdownPlaceholderText: 'Try "Javascript"',
      expandInput: true,
      source: function (autocomplete, query, render) {
        let results = []
        if (query.length === 0) {
          render(results)
          return
        }
        autocomplete.showPreloader()
        self.$$.ajax({
          url: '/static/data/autocomplete-languages.json',
          method: 'GET',
          dataType: 'json',
          data: {
            query: query
          },
          success: function (data) {
            for (let i = 0; i < data.length; i++) {
              if (data[i].name.toLowerCase().indexOf(query.toLowerCase()) >= 0) {
                results.push(data[i])
              }
            }
            autocomplete.hidePreloader()
            render(results)
          }
        })
      }
    })
    let autocompleteStandaloneSimple = this.$f7.autocomplete({
      openIn: 'page',
      opener: self.$$('#autocomplete-standalone'),
      backOnSelect: true,
      source: function (autocomplete, query, render) {
        let results = []
        if (query.length === 0) {
          render(results)
          return
        }
        for (let i = 0; i < fruits.length; i++) {
          if (fruits[i].toLowerCase().indexOf(query.toLowerCase()) >= 0) {
            results.push(fruits[i])
          }
        }
        render(results)
      },
      onChange: function (autocomplete, value) {
        self.standaloneFruit = value[0]
      }
    })
    let autocompleteStandalonePopup = this.$f7.autocomplete({
      openIn: 'popup',
      opener: self.$$('#autocomplete-popup'),
      backOnSelect: true,
      source: function (autocomplete, query, render) {
        let results = []
        if (query.length === 0) {
          render(results)
          return
        }
        for (let i = 0; i < fruits.length; i++) {
          if (fruits[i].toLowerCase().indexOf(query.toLowerCase()) >= 0) {
            results.push(fruits[i])
          }
        }
        render(results)
      },
      onChange: function (autocomplete, value) {
        self.popupFruit = value[0]
      }
    })
    let autocompleteStandaloneMulti = this.$f7.autocomplete({
      openIn: 'page',
      opener: self.$$('#autocomplete-multiple'),
      multiple: true,
      source: function (autocomplete, query, render) {
        let results = []
        if (query.length === 0) {
          render(results)
          return
        }
        for (let i = 0; i < fruits.length; i++) {
          if (fruits[i].toLowerCase().indexOf(query.toLowerCase()) >= 0) {
            results.push(fruits[i])
          }
        }
        render(results)
      },
      onChange: function (autocomplete, value) {
        self.multiFruit = value.join(', ')
      }
    })
    let autocompleteStandaloneAjax = this.$f7.autocomplete({
      openIn: 'page',
      opener: self.$$('#autocomplete-standalone-ajax'),
      multiple: true,
      valueProperty: 'id',
      textProperty: 'name',
      limit: 50,
      preloader: true,
      source: function (autocomplete, query, render) {
        let results = []
        if (query.length === 0) {
          render(results)
          return
        }
        autocomplete.showPreloader()
        self.$$.ajax({
          url: '/static/data/autocomplete-languages.json',
          method: 'GET',
          dataType: 'json',
          data: {
            query: query
          },
          success: function (data) {
            for (let i = 0; i < data.length; i++) {
              if (data[i].name.toLowerCase().indexOf(query.toLowerCase()) >= 0) {
                results.push(data[i])
              }
            }
            autocomplete.hidePreloader()
            render(results)
          }
        })
      },
      onChange: function (autocomplete, value) {
        let itemText = [],
            inputValue = []
        for (let i = 0; i < value.length; i++) {
          itemText.push(value[i].name)
          inputValue.push(value[i].id)
        }
        self.ajaxLanguageTitle = itemText.join(', ')
        self.ajaxLanguage = inputValue.join(', ')
      }
    })
  }
}
</script>

<style lang="less">
</style>
