<template>

    <apexchart type="heatmap" width="250" height="200"  :options="chartOptions" :series="series"></apexchart>
  
</template>

<script>
export default {
	name: 'chartMap',
  data() {
    return {
      chartOptions: {
        chart: {
          height: 350,
          type: 'heatmap',
        },
        dataLabels: {
          enabled: false
        },
        colors: ["#008FFB"],
        xaxis: {
          type: 'category',
          categories: ['Segunda', 'Terça', 'Quarta', 'Quinta', 'Sexta']
        },
        title: {
          text: 'Atividades diárias'
        },
        grid: {
          padding: {
            right: 10
          }
        }
      },
      series: [
        {
          name: 'Acordar Cedo',
          data: this.generateDayData()
        },
        {
          name: 'Fazer Exercícios',
          data: this.generateDayData()
        },
        {
          name: 'Tomar Chimarrão',
          data: this.generateDayData()
        }
      ]
    }
  },
  methods: {
    generateDayData() {
      let data = []
      for (let i = 0; i < 5; i++) {
        data.push({
          x: `Dia ${i + 1}`,
          y: Math.floor(Math.random() * 10)
        })
      }
      return data
    }
  }
}
</script>