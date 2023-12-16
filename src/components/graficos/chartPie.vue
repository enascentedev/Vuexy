<template>
	<!-- tirar legendas -->
  <div>
    <apexchart type="area" width="230" height="220" :options="chartOptions" :series="series"></apexchart>
  </div>
</template>

<script>
export default {
	name: "chartPie",
  data() {
    return {
      chartOptions: {

				//eixo x
        xaxis: {
          type: 'category',
          categories: ['Jun', 'Jul', 'Ago', 'Set', 'Out', 'Nov', 'Dez']
        },

				// stepline, smooth,straight
        stroke: {
          curve: 'smooth'
        },
				//legend
        dataLabels: {
          enabled: false
        },

				// opacity cors
        fill: {
          type: 'gradient',
          gradient: {
            shadeIntensity: 1,
            opacityFrom: 0.7,
            opacityTo: 0.9,
            stops: [0, 90, 100]
          }
        }
      },

			//eixo y
      series: [{
        name: 'series1',
        data: [31, 40, 28, 51, 42, 109, 100]
      }]
    }
  }
}
</script>
