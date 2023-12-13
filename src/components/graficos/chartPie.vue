<template>
	<!-- tirar legendas -->
  <div>
    <apexchart type="area" width="180" height="220" :options="chartOptions" :series="series"></apexchart>
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

				//acentuamento da curva opções: stepline, smooth,straight
        stroke: {
          curve: 'smooth'
        },
				//mostra legenda no gráfico
        dataLabels: {
          enabled: false
        },

				//opacidade das cores
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
