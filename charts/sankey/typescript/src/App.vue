<template>
  <div id="app">
    <chart-sankey :data="chartData"></chart-sankey>
  </div>
</template>

<script>
import { ChartSankey } from 'vue-d2b';

export default {
  name: 'App',

  data () {
    return {
      chartData: {
        // This is the top x-axis
        // These properties apply to the rest of the axes (x2, y, y2)
        x: {
          label: 'bottom x-axis label',
          labelOrient: 'inner end',
          linearPadding: [-0.11, 0.22],
          orient: 'inner',
          scale: {

          },
          showGrid: false,
          // tickFormat: format(',.0f'),
          // The padding between the tick marks and the tick values
          tickPadding: 50,
          // The length of the tick marks
          tickSize: 50,
          // To choose which tick values are shown along the axiss
          tickValues: [1, 5, 8, 12, 3],
          ticks: (20, 'f')      
        },
        // These are the different data sets that will be displayed in the chart
        sets: [
          {
            // The types of graphs that can be generated
            generators: [{types:['area', 'line', 'scatter']}],
            // The actual data sets for the graphs 
            graphs: [
              {
                // The title for an area graph
                label: 'Area 1',
                // The data points that will be used to generate the area graph
                values: [
                  { x: 1, y: 15 },
                  { x: 2, y: 18 },
                  { x: 3, y: 14 },
                  { x: 4, y: 10 },
                  { x: 5, y: 12 }
                ]
              },
              {
                label: 'Area 2',
                values: [
                  { x: 1, y: 11 },
                  { x: 2, y: 10 },
                  { x: 3, y: 18 },
                  { x: 4, y: 1 },
                  { x: 5, y: 12 }
                ]
              }
            ]
          }
        ]
      }
    }
  },

  components: {
    ChartSankey
  }
};
</script>

<style scoped>
#app {
  width: 100%;
  height: 100%;
}
</style>
