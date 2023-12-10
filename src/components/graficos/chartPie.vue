<template>
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
        chart: {
          height: 'auto'
        },
        xaxis: {
          type: 'category',
          categories: ['Jun', 'Jul', 'Ago', 'Set', 'Out', 'Nov', 'Dez']
        },
        stroke: {
          curve: 'smooth'
        },
        dataLabels: {
          enabled: false
        },
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
      series: [{
        name: 'series1',
        data: [31, 40, 28, 51, 42, 109, 100]
      }]
    }
  }
}
</script>
