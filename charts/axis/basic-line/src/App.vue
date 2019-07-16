<template>
  <div id="app">
    <chart-axis :data="chartData"></chart-axis>
  </div>
</template>

<script>
import { ChartAxis } from 'vue-d2b';

export default {
  name: 'App',

  data () {
    return {
      chartData: {
        sets: [
			  {
				generators: [{
					types: ['line', 'scatter']
				}],
				graphs: [
			    {
			      label: 'Line 1',
			      values: [
			        {x: 1, y: 25},
			        {x: 2, y: 38},
			        {x: 3, y: 24},
			        {x: 4, y: 60},
			        {x: 5, y: 22}
			      ]
			    },
			    {
			    	label: 'Line 2',
			    	values: [
			      	{x: 1, y: 41},
			      	{x: 2, y: 60},
			      	{x: 3, y: 18},
			      	{x: 4, y: 5},
			      	{x: 5, y: 12}
			      ]
			    }
				]
			}
		]
	}
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
