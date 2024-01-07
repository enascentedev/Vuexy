<template>
  <div>
    <apexchart :options="chartOptions" :series="chartSeries" type="bar" width="400" />
  </div>
</template>

<script>
import VueApexCharts from 'vue3-apexcharts';

export default {
  name: 'ChartBar',
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      chartOptions: {
        series: [
          {
            name: 'coins',
            data: [2, 4, 3, 4, 3, 5, 5, 6.5, 6, 5, 4, 5, 8, 7, 7, 8, 8, 10, 9, 9, 12, 12, 11, 12, 13, 14, 16, 14, 15, 17, 19, 21]
          }
        ],
        chart: {
          type: 'bar',
          height: 410,
          animations: {
            enabled: false
          }
        },
        plotOptions: {
          bar: {
            horizontal: true,
            barHeight: '100%',
          },
        },
        dataLabels: {
          enabled: false,
        },
        stroke: {
          colors: ["#fff"],
          width: 0.2
        },
        labels: Array.apply(null, { length: 39 }).map(function (el, index) {
          return index + 1;
        }),
        yaxis: {
          axisBorder: {
            show: false
          },
          axisTicks: {
            show: false
          },
          labels: {
            show: false
          },
          title: {
            text: 'Weight',
          },
        },
        grid: {
          position: 'back'
        },
        title: {
          text: 'Paths filled by clipped image',
          align: 'right',
          offsetY: 30
        },
        fill: {
          type: 'image',
          opacity: 0.87,
          image: {
            src: [
              'https://static.todamateria.com.br/upload/pa/is/paisagem-natural-og.jpg',
              'https://static.todamateria.com.br/upload/pa/is/paisagem-natural-og.jpg',
              'https://static.todamateria.com.br/upload/pa/is/paisagem-natural-og.jpg',
              // Adicione mais URLs conforme necessário
            ],
            width: 466,
            height: 406
          }
        },
      },
      chartSeries: ['coins'],
    };
  },
};
</script>
