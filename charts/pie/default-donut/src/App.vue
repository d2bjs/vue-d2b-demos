<template>
  <div id="app">
    <chart-pie :data="chartData"></chart-pie>
  </div>
</template>

<script>
import { ChartDonut } from 'vue-d2b';

export default {
  name: 'App',

  data () {
    return {
      chartData: 
        [
        {label: 'arc 1', value: 23},
        {label: 'arc 2', value: 31},
        {label: 'arc 3', value: 80},
        {label: 'arc 4', value: 8}
        ],
        donutRatio: 0.5
      }
  },

  components: {
    ChartAxis
  }
};
</script>

<style scoped>
#app {
  width: 100%;
  height: 100%;
}
</style>
