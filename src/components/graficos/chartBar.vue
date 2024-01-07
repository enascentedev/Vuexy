<template>
  <div>
    <apexchart type="area" width="460" height="200" :options="chartOptions" :series="chartSeries" />
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
        chart: {
          type: 'area',
          height: 350,
					toolbar: {
            show: false,
          },
        },
        dataLabels: {
          enabled: false,
        },
        stroke: {
          curve: 'smooth',
        },
        xaxis: {
          categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
        },
        tooltip: {
          x: {
            format: 'MMM',
          },
        },
      },
      chartSeries: [
        {
          name: 'Series 1',
          data: [30, 40, 25, 50, 49, 21, 70, 51, 60, 75, 30, 40],
        },
        {
          name: 'Series 2',
          data: [23, 12, 54, 61, 32, 56, 81, 19, 45, 30, 60, 80],
        },
      ],
    };
  },
};
</script>
