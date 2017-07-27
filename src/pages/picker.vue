<template>
  <f7-page>
    <f7-navbar title="Picker" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-block>
      <p>
        Picker is a powerful component that allows you to create custom overlay pickers which looks like iOS native picker.
      </p>
      <p>
        Picker could be used as inline component or as overlay. Overlay Picker will be automatically converted to Popover on tablets (iPad).
      </p>
    </f7-block>
    <f7-block-title>PICKER WITH SINGLE VALUE</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Your iOS device" id="picker-device"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>2 VALUES AND 3D-ROTATE EFFECT</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Descripe yourself" id="picker-descripe"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>DEPENDENT VALUES</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Your car" id="picker-dependent"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>CUSTOM TOOLBAR</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" placeholder="Descripe yourself" id="picker-csutom"></f7-input>
      </f7-list-item>
    </f7-list>
    <f7-block-title>INLINE PICKER / DATE-TIME</f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-input type="text" id="picker-date"></f7-input>
      </f7-list-item>
      <div class="content-block-inner">
        <div id="picker-date-container"></div>
      </div>
    </f7-list>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      carVendors: {
        Japanese : ['Honda', 'Lexus', 'Mazda', 'Nissan', 'Toyota'],
        German : ['Audi', 'BMW', 'Mercedes', 'Volkswagen', 'Volvo'],
        American : ['Cadillac', 'Chrysler', 'Dodge', 'Ford']
      }
    }
  },
  mounted () {
    let self = this

    let pickerDevice = self.$f7.picker({
      input: '#picker-device',
      cols: [
        {
          textAlign: 'center',
          values: ['iPhone 4', 'iPhone 4S', 'iPhone 5', 'iPhone 5S', 'iPhone 6', 'iPhone 6 Plus', 'iPad 2', 'iPad Retina', 'iPad Air', 'iPad mini', 'iPad mini2', 'iPad mini3']
        }
      ]
    })
    
    let pickerDescripe = self.$f7.picker({
      input: '#picker-descripe',
      rotateEffect: true,
      cols: [
        {
          textAlign: 'left',
          values: ('Super Lex Amazing Bat Iron Rocket Lex Cool Beautiful Wonderful Raining Happy Amazing Funny Cool Hot').split(' ')
        }, {
          values: ('Man Luthor Woman Boy Girl Person Cutie Babe Raccoon').split(' ')
        },
      ]
    })

    let pickerDependent = self.$f7.picker({
      input: '#picker-dependent',
      rotateEffect: true,
      formatValue: function (picker, values) {
        return values[1]
      },
      cols: [
        {
          textAlign: 'left',
          values: ['Japanese', 'German', 'American'],
          onChange: function (picker, country) {
            if (picker.cols[1].replaceValues) {
              picker.cols[1].replaceValues(self.carVendors[country])
            }
          }
        }, {
          values: self.carVendors.Japanese,
          width: 160
        }
      ]
    })

    let pickerCustom = self.$f7.picker({
      input: '#picker-csutom',
      rotateEffect: true,
      toolbarTemplate: 
        '<div class="toolbar">' + 
          '<div class="toolbar-inner">' + 
            '<div class="left">' + 
              '<a href="#" class="link toolbar-randomize-link">Randomize</a>' +
            '</div>' +
            '<div class="right">' +
              '<a href="#" class="link close-picker">That\'s me</a>' +
            '</div>' +
          '</div>' +
        '</div>',
      cols: [
        {
          values: ['Mr', 'Ms']
        }, {
          textAlign: 'left',
          values: ('Super Lex Amazing Bat Iron Rocket Lex Cool Beautiful Wonderful Raining Happy Amazing Funny Cool Hot').split(' ')
        }, {
          values: ('Man Luthor Woman Boy Girl Person Cutie Babe Raccoon').split(' ')
        }
      ],
      onOpen: function (picker) {
        picker.container.find('.toolbar-randomize-link').on('click', function () {
          let col0Values = picker.cols[0].values
          let col0Random = col0Values[Math.floor(Math.random() * col0Values.length)]

          let col1Values = picker.cols[1].values
          let col1Random = col1Values[Math.floor(Math.random() * col1Values.length)]

          let col2Values = picker.cols[2].values
          let col2Random = col2Values[Math.floor(Math.random() * col2Values.length)]

          picker.setValue([col0Random, col1Random, col2Random])
        })
      }
    })

    let today = new Date()
    let pickerInline = self.$f7.picker({
      input: '#picker-date',
      container: '#picker-date-container',
      toolbar: false,
      rotateEffect: true,

      value: [today.getMonth(), today.getDate(), today.getFullYear(), today.getHours(), (today.getMinutes() < 10 ? '0' + today.getMinutes() : today.getMinutes())],

      onChange: function (picker, values, displayValues) {
        let dayInMonth = new Date(picker.value[2], picker.value[0] * 1 + 1, 0).getDate()
        if (values[1] > dayInMonth) {
          picker.cols[1].setValue(dayInMonth)
        }
      },

      formatValue: function (p, values, displayValues) {
        return displayValues[0] + ' ' + values[1] + ', ' + values[2] + ' ' + values[3] + ':' + values[4]
      },

      cols: [
        // Months
        {
          values: ('0 1 2 3 4 5 6 7 8 9 10 11').split(' '),
          displayValues: ('January February March April May June July August September October November December').split(' '),
          textAlign: 'left'
        },
        // Days
        {
          values: [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31],
        },
        // Years
        {
          values: (function () {
            var arr = [];
            for (var i = 1950; i <= 2030; i++) { arr.push(i); }
            return arr;
          })(),
        },
        // Space divider
        {
          divider: true,
          content: '  '
        },
        // Hours
        {
          values: (function () {
            var arr = [];
            for (var i = 0; i <= 23; i++) { arr.push(i); }
            return arr;
          })(),
        },
        // Divider
        {
          divider: true,
          content: ':'
        },
        // Minutes
        {
          values: (function () {
            var arr = [];
            for (var i = 0; i <= 59; i++) { arr.push(i < 10 ? '0' + i : i); }
            return arr;
          })(),
        }
      ]
    })
  }
}
</script>

<style lang="less">

</style>
