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
      nodes: [
        {name: 'Node A'},
        {name: 'Node B'},
        {name: 'Node C'},
        {name: 'Node D'},
        {name: 'Node E'},
      ],
      links: [
        {source: 'Node A', target: 'Node E', value: 2},
        {source: 'Node A', target: 'Node C', value: 2},
        {source: 'Node B', target: 'Node C', value: 2},
        {source: 'Node B', target: 'Node D', value: 2},
        {source: 'Node C', target: 'Node D', value: 2},
        {source: 'Node C', target: 'Node E', value: 2},
        {source: 'Node D', target: 'Node E', value: 4},
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
