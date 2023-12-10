<template>
  <div>
    <apexchart
      type="radialBar"
      width="180" height="220"
      :options="chartOptions"
      :series="series"
    ></apexchart>
  </div>
</template>

<script>
import VueApexCharts from 'vue3-apexcharts';

export default {
  name: 'chartRadial',
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      series: [85],
      chartOptions: {
        chart: {
          height: 350,
          type: 'radialBar',
        },
        plotOptions: {
          radialBar: {
            hollow: {
              size: '70%',
            },
            dataLabels: {
              showOn: 'always',
              name: {
                offsetY: -10,
                show: true,
                color: '#888',
                fontSize: '13px'
              },
              value: {
                color: '#111',
                fontSize: '30px',
                show: true,
                formatter: function (val) {
                  return val + '%';
                }
              }
            }
          }
        },
        labels: ['Tarefas completas'],
       
        legend: {
          show: true,
          floating: true,
          position: 'bottom',
          offsetX: 0,
          offsetY: 5,
          labels: {
            useSeriesColors: true,
          },
          markers: {
            size: 0
          },
          formatter: function(seriesName, opts) {
            return seriesName + ': ' + opts.w.globals.series[opts.seriesIndex]
          },
          itemMargin: {
            horizontal: 3,
          },
        },
      },
    };
  },
};
</script>
