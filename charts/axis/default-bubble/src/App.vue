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
		x: {
			linearPadding: [-0.1, 0.1],
			label: 'Some X Label',
		},
		sets: [{
				generators: [{types: ["bubblePack"]}],
				graphs: [
				    { hidden: false,
              label: 'bubble pack 1',
              values: [
                {
                  label: 'one',
                  children: [
                    {
                      label: 'one-one',
                      size: 5,
                      x: 7,
                      y: 25
                    }
                  ]
                },
                {
                  expanded: true,
                  label: 'two',
                  children: [
                    {
                      label: 'two-one',
                      size: 5,
                      x: 3,
                      y: 15
                    },
                    {
                      label: 'two-two',
                      children: [
                        {
                          label: 'two-two-one',
                          size: 2,
                          x: 6,
                          y: 8
                        },
                        {
                          label: 'two-two-two',
                          size: 17,
                          x: 8,
                          y: 21
                        }
                      ]
                    }
                  ]
                }
              ]
            }
				]
		}]
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
