<template>
  <div>
    <apexchart type="radialBar" width="350" height="250" :options="chartOptions" :series="series"></apexchart>
  </div>
</template>

<script>
import VueApexCharts from 'vue3-apexcharts';

export default {
  name: 'chartMap',
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      series: [76, 67, 61, 90],
      chartOptions: {
        chart: {
          height: 220,
          type: 'radialBar',
        },
        plotOptions: {
          radialBar: {
          
            dataLabels: {
              show: true, 
              name: {
                show: true,
                fontSize: '16px',
                fontFamily: undefined,
                color: undefined,
                offsetY: -10
              },
              value: {
                show: true, 
                fontSize: '14px',
                fontFamily: undefined,
                color: undefined,
                offsetY: 5,
                formatter: function (val) {
                  return val; 
                }
              },
              total: {
                show: true,
                label: 'Total',
                formatter: function (w) {
                  const sum = w.globals.seriesTotals.reduce((total, num) => {
                    return total + num;
                  }, 0);
                  return sum;
                }
              }
            }
          }
        },
        labels: ['Twiter', 'Messenger', 'Facebook', 'LinkedIn'],
        colors: ['#45A1FF', '#2C7BE5', '#2E93fA', '#4E73DF'],
        legend: {
          show: false, 
          position: 'bottom',
        },
        responsive: [{
          breakpoint: 480,
          options: {
            chart: {
              width: 300
            },
            legend: {
              position: 'bottom'
            },
          }
        }],
      },
    };
  },
};
</script>
