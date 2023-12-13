<template>
  <div id="chart-container" ref="chartContainer" class="relative">
    <apexchart
      type="pie"
      :options="chartOptions"
      :series="series"
    ></apexchart>
    <img
      v-for="(logo, index) in logos"
      :key="index"
      :src="logo.src"
      :class="`logo-${index}`"
      :alt="`Logo ${index + 1}`"
      class="logo"
    />
  </div>
</template>

<script>
import VueApexCharts from 'vue-apexcharts';
export default {
	name:'ChartBrand',
  components: {
    apexchart: VueApexCharts,
  },
  data() {
    return {
      series: [25.6, 25.0, 30.7, 18.8],
      chartOptions: {
        labels: ['series-1', 'series-2', 'series-3', 'series-4'],
        // outras opções de configuração...
      },
      logos: [
        { src: 'https://img.ws.mms.shopee.com.br/ec926f6bba30904954ce4dfe245afb0d', top: 0, left: 0 },
        { src: 'https://img.ws.mms.shopee.com.br/ec926f6bba30904954ce4dfe245afb0d', top: 0, left: 0 },
        { src: 'https://img.ws.mms.shopee.com.br/ec926f6bba30904954ce4dfe245afb0d', top: 0, left: 0 },
      ],
    };
  },
  mounted() {
    this.positionLogos();
  },
  methods: {
    positionLogos() {
      const total = this.series.reduce((a, b) => a + b, 0);
      let currentAngle = -90; // Começar do topo do círculo

      this.logos.forEach((logo, index) => {
        const sliceAngle = (this.series[index] / total) * 360;
        const angleRad = (currentAngle + (sliceAngle / 2)) * (Math.PI / 180);

        const chartRect = this.$refs.chartContainer.getBoundingClientRect();
        const chartRadius = chartRect.width / 2; // Supondo que o gráfico é um círculo perfeito

        // Posição do centro da imagem
        const imageCenterX = chartRect.left + chartRadius + (chartRadius * Math.cos(angleRad));
        const imageCenterY = chartRect.top + chartRadius + (chartRadius * Math.sin(angleRad));

        // Ajuste para posicionar a imagem sobre o slice, considerando o tamanho da imagem
        const imageSize = 700; // Tamanho da imagem (assumindo que é quadrada)
        logo.top = imageCenterY - (imageSize / 2); // Centro da imagem no slice
        logo.left = imageCenterX - (imageSize / 2); // Centro da imagem no slice

        currentAngle += sliceAngle;
      });
    },
  },
};
</script>

<style>
#chart-container {
  @apply w-full md:w-1/2 lg:w-1/3 h-auto;
}

.logo {
  @apply absolute transform -translate-x-1/2 -translate-y-1/2;
  width: 100px; /* ou qualquer tamanho que seja apropriado para o seu design */
  height: 100px; /* ou qualquer tamanho que seja apropriado para o seu design */
}
</style>
