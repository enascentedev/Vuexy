<template>
  <div>
    <apexchart type="bar" width="260" height="220" :options="chartOptions" :series="series"></apexchart>
   
  </div>
</template>

<script>
import VueApexCharts from 'vue3-apexcharts';

export default {
  name: 'EarningsChart',
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      series: [{
        data: [44, 55, 41, 64, 22, 43, 21]
      }],
      chartOptions: {
        chart: {
          type: 'bar',
          height: 350
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
        xaxis: {
          categories: ['Seg', 'Ter', 'Qua', 'Qui', 'Sex', 'Sab', 'Dom'],
        },
        colors: ['#8E54E9'],
        fill: {
          colors: ['#8E54E9', '#2b908f']
        },
        legend: {
          show: true, 
        },
        
      },
    };
  },
};
</script>

<style scoped>
.legenda {
  @apply flex flex-col;
}

.legenda-item {
  @apply flex items-center my-2;
}

</style>
