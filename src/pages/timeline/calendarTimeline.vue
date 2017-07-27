<template>
  <f7-page name="calendar-timeline">
    <f7-navbar title="Calendar Timeline" back-link="Back" sliding>
      <f7-nav-right>
        <f7-link icon="icon icon-bars" open-panel="left"></f7-link>
      </f7-nav-right>
    </f7-navbar>
    <f7-timeline horizontal col="33" tablet-col="20">
      <f7-timeline-year v-for="year in calendar" :title="year.year" :key="year">
        <f7-timeline-month v-for="month in year.months" :title="month.month" :key="year + month">
          <f7-timeline-item v-for="day in month.days" :date="day.day" :key="year + month + day">
            <f7-timeline-item-child v-for="(task, index) in day.tasks"
              :time="task.time"
              :text="task.text"
              :key="index"
            ></f7-timeline-item-child>
          </f7-timeline-item>
        </f7-timeline-month>
      </f7-timeline-year>
    </f7-timeline>
  </f7-page>
</template>

<script>
export default {
  data () {
    return {
      calendar: [
        {
          year: 2016,
          months: [
            {
              month: 'November',
              days: [
                {
                  day: '20',
                  tasks: [
                    {
                      time: '6:00',
                      text: 'Task 1'
                    }, {
                      time: '11:00',
                      text: 'Task 2'
                    }
                  ]
                }, {
                  day: '21',
                  tasks: [
                    {
                      time: '12:00',
                      text: 'Task 1'
                    }, {
                      time: '2:00',
                      text: 'Task 2'
                    }, {
                      time: '15:00',
                      text: 'Task 3'
                    }
                  ]
                }, {
                  day: '22',
                  tasks: [
                    {
                      time: '4:00',
                      text: 'Task 1'
                    }, {
                      time: '2:00',
                      text: 'Task 2'
                    }, {
                      time: '7:00',
                      text: 'Task 3'
                    }, {
                      time: '5:00',
                      text: 'Task 4'
                    }
                  ]
                }, {
                  day: '23',
                  tasks: [
                    {
                      time: '17:00',
                      text: 'Task 1'
                    }, {
                      time: '7:00',
                      text: 'Task 2'
                    }
                  ]
                }, {
                  day: '24',
                  tasks: [
                    {
                      time: '18:00',
                      text: 'Task 1'
                    }, {
                      time: '5:00',
                      text: 'Task 2'
                    }
                  ]
                }, {
                  day: '25',
                  tasks: [
                    {
                      time: '5:00',
                      text: 'Task 1'
                    }, {
                      time: '20:00',
                      text: 'Task 2'
                    }, {
                      time: '20:00',
                      text: 'Task 3'
                    }
                  ]
                }, {
                  day: '26',
                  tasks: [
                    {
                      time: '8:00',
                      text: 'Task 1'
                    }, {
                      time: '22:00',
                      text: 'Task 2'
                    }
                  ]
                }, {
                  day: '27',
                  tasks: [
                    {
                      time: '20:00',
                      text: 'Task 1'
                    }, {
                      time: '7:00',
                      text: 'Task 2'
                    }, {
                      time: '8:00',
                      text: 'Task 3'
                    }, {
                      time: '10:00',
                      text: 'Task 4'
                    }
                  ]
                }, {
                  day: '28',
                  tasks: [
                    {
                      time: '14:00',
                      text: 'Task 1'
                    }, {
                      time: '14:00',
                      text: 'Task 2'
                    }
                  ]
                }, {
                  day: '29',
                  tasks: [
                    {
                      time: '17:00',
                      text: 'Task 1'
                    }
                  ]
                }, {
                  day: '30',
                  tasks: [
                    {
                      time: '19:00',
                      text: 'Task 1'
                    }, {
                      time: '6:00',
                      text: 'Task 2'
                    }
                  ]
                }, {
                  day: '31',
                  tasks: [
                    {
                      time: '0:00',
                      text: 'Task 1'
                    }, {
                      time: '8:00',
                      text: 'Task 2'
                    }
                  ]
                }
              ]
            }
          ]
        }, {
          year: 2017,
          months: [
            {
              month: 'January',
              days: [
                {
                  day: '1',
                  tasks: [
                    {
                      time: '11:00',
                      text: 'Task 1'
                    }, {
                      time: '10:00',
                      text: 'Task 2'
                    }, {
                      time: '14:00',
                      text: 'Task 3'
                    }
                  ]
                }, {
                  day: '2',
                  tasks: [
                    {
                      time: '9:00',
                      text: 'Task 1'
                    }, {
                      time: '5:00',
                      text: 'Task 2'
                    }, {
                      time: '12:00',
                      text: 'Task 3'
                    }, {
                      time: '23:00',
                      text: 'Task 4'
                    }
                  ]
                }, {
                  day: '3',
                  tasks: [
                    {
                      time: '16:00',
                      text: 'Task 1'
                    }, {
                      time: '9:00',
                      text: 'Task 2'
                    }
                  ]
                }, {
                  day: '4',
                  tasks: [
                    {
                      time: '21:00',
                      text: 'Task 1'
                    }
                  ]
                }, {
                  day: '5',
                  tasks: [
                    {
                      time: '16:00',
                      text: 'Task 1'
                    }, {
                      time: '22:00',
                      text: 'Task 2'
                    }, {
                      time: '8:00',
                      text: 'Task 3'
                    }
                  ]
                }, {
                  day: '6',
                  tasks: [
                    {
                      time: '8:00',
                      text: 'Task 1'
                    }
                  ]
                }, {
                  day: '7',
                  tasks: [
                    {
                      time: '5:00',
                      text: 'Task 1'
                    }, {
                      time: '8:00',
                      text: 'Task 2'
                    }, {
                      time: '5:00',
                      text: 'Task 3'
                    }
                  ]
                }, {
                  day: '8',
                  tasks: [
                    {
                      time: '19:00',
                      text: 'Task 1'
                    }, {
                      time: '9:00',
                      text: 'Task 2'
                    }
                  ]
                }
              ]
            }
          ]
        }
      ]
    }
  }
}
</script>

<style lang="less">
.page[data-page="calendar-timeline"]{
  .timeline-item-child{
    margin-top: 15px;

    &:first-child{
      margin-top: 0;
    }
  }
}
</style>
