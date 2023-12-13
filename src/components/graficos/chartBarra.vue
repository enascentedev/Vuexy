<template>
  <div>
    <apexchart type="bar" width="260" height="220" :options="chartOptions" :series="series"></apexchart>
   
  </div>
</template>

<script>
import VueApexCharts from 'vue3-apexcharts';

export default {
  name: 'ChartBarra',
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
			// Dados para o gráfico
      series: [{
        data: [44, 55, 41, 64, 22, 43, 21]
      }],

			// Opções de configuração do gráfico
      chartOptions: {
        chart: {
          type: 'bar',
        },

        plotOptions: {
          bar: {
            borderRadius: 4,
            horizontal: false,
          }
        },
        dataLabels: {
          enabled: false
        },

				//config eixo x
        xaxis: {
          categories: ['Seg', 'Ter', 'Qua', 'Qui', 'Sex', 'Sab', 'Dom'],
        },
        colors: ['#8E54E9'],
        fill: {
          colors: ['#8E54E9', '#2b908f']
        },
        legend: {
          show: false, 
        },
        
      },
    };
  },
};
</script>
