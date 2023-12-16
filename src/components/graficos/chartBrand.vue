<template>
  <div>
    <apexchart type="donut" width="340" height="220" :options="chartOptions" :series="series"></apexchart>
  </div>
</template>

<script>
import VueApexCharts from 'vue3-apexcharts';

export default {
	name: "chartBrand",
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {

      series: [44, 55, 13, 33, 22, 44],

      chartOptions: {
        chart: {
          width: 380,
          type: 'donut',
        },
        labels: ['Loja 1', 'Loja 2', 'Loja 3', 'Loja 4', 'Loja 5', 'Loja 6'], 
        dataLabels: {
          enabled: true
        },
        legend: {
          show: true
        },
        fill: {
          type: 'gradient',
          gradient: {
            shadeIntensity: 1,
            opacityFrom: 0.7,
            opacityTo: 0.9,
            stops: [0, 90, 100]
          }
        },
        responsive: [{
          breakpoint: 480,
          options: {
            chart: {
              width: 200
            },
            legend: {
              show: true,
							position: 'bottom',
            }
          }
        }],
      },
    }
  }
}
</script>
