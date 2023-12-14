<template>
  <div>
    <apexchart type="donut" width="300" :options="chartOptions" :series="series"></apexchart>
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
      // Dados da série agora são apenas um array de números
      series: [44, 55, 13, 33, 22, 44, 67],

      // Opções de configuração do gráfico de rosca
      chartOptions: {
        chart: {
          width: 380,
          type: 'donut',
        },
        labels: ['Series 1', 'Series 2', 'Series 3', 'Series 4', 'Series 5', 'Series 6', 'Series 7'], // Pode adicionar labels correspondentes aqui
        dataLabels: {
          enabled: false
        },
        legend: {
          show: false // Isto remove as legendas
        },
        fill: {
          type: 'gradient',
          gradient: {
            // Configurações de gradiente podem ser ajustadas conforme necessário
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
              show: false
            }
          }
        }],
      },
    }
  }
}
</script>
