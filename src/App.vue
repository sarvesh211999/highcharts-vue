<template>
  <div>
    <one :options="options"></one>
    <two :options="options"></two>

  </div>
</template>

<script>
import one from 'vue2-highcharts'
import two from 'vue2-highcharts'

const asyncData = {
  name: 'Tokyo',
  marker: {
    symbol: 'square'
  },
  data: [7.0, 6.9, 9.5, 14.5, 18.2, 21.5, 25.2, {
    y: 26.5,
    marker: {
      symbol: 'url(http://www.highcharts.com/demo/gfx/sun.png)'
    }
  }, 23.3, 18.3, 13.9, 9.6]
}
export default{
    components: {
        one,
        two
    },
    data(){
      return{
        options: {
          chart: {
            type: 'spline'
          },
          title: {
            text: 'Monthly Average Temperature'
          },
          subtitle: {
            text: 'Source: WorldClimate.com'
          },
          xAxis: {
            categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun',
              'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec']
          },
          yAxis: {
            title: {
              text: 'Temperature'
            },
          },
          series: [{
            name: 'Jane',
            data: [1, 0, 4]
          }, {
            name: 'John',
            data: [1 ,1 ,1, 1 ,1 ,1, 1 ,1 ,3, 1 ,2 ,3]
          }]
        }
      }
    },

};
</script>