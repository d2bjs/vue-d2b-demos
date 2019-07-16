<template>
  <div id="app">
    <chart-sunburst :data="chartData"></chart-sunburst>
  </div>
</template>

<script>
import { ChartSunburst } from 'vue-d2b';

export default {
  name: 'App',

  data () {
    return {
      chartData: {
        label: 'root',
        children: [
          {
          label: 'child 1',
          children: [
            {
            label: 'child 1-1',
            size: 10
            },
            {
            label: 'child 1-2',
            children: [
              {
              label: 'child 1-2-1',
              size: 5
              },
              {
              label: 'child 1-3-1',
              size: 8
              }
            ]
            },
            {
            label: 'child 1-3',
            // selected: true,
            children: [
              {
              label: 'child 1-3-1',
              children: [
                {
                label: 'child 1-3-1-1',
                size: 2
                },
                {
                label: 'child 1-3-1-2',
                size: 16
                }
              ]
              },
              {
              label: 'child 1-3-2',
              size: 8
              }
            ]
            }
          ]
          },
          {
          label: 'child 2',
          size: 25
          }
        ]
      }
    }
  },

  components: {
    ChartSunburst
  }
};
</script>

<style scoped>
#app {
  width: 100%;
  height: 100%;
}
</style>
