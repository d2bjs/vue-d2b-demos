<template>
  <div id="app">
    <chart-pie :data="chartData"></chart-pie>
  </div>
</template>

<script>
import { ChartPie } from 'vue-d2b';

export default {
  name: 'App',

  data () {
    return { 
      chartData: 
        [
        {label: 'arc 1', value: 23, ratio: 0.5},
        {label: 'arc 2', value: 31, ratio: 0.5},
        {label: 'arc 3', value: 80, ratio: 0.5},
        {label: 'arc 4', value: 68, ratio: 0.5}
        ],
    }
  },

  components: {
    ChartPie
  }
};
</script>

<style scoped>
#app {
  width: 100%;
  height: 100%;
}
</style>
