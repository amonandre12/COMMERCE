<template>
  <div class="container">
    <Bar
      id="my-chart-id"
      :options="chartOptions"
      :data="chartData"
    />
  </div>
</template>

<script>
import { Bar } from 'vue-chartjs';
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  BarElement,
  CategoryScale,
  LinearScale,
} from 'chart.js';
// import { name } from '@vue/eslint-config-prettier/skip-formatting';

// Enregistre les composants nécessaires pour Chart.js
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale);

export default {
  name: 'BarChart',
  components: { Bar },
  data() {
    return {
      chartData: {
        labels: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
        datasets: [
          {
            data: [50, 60, 80, 70, 20, 30, 50, 60, 40, 50, 60, 70],
            backgroundColor: '#333F',
            borderRadius: 5,
          },
        ],
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        plugins: {
          legend: {
            display: true,
            position: 'top',
          },
        },
        scales: {
          y: {
            beginAtZero: true,
            ticks: {
              stepSize: 20,
              callback: (value) => {
                if (value === 0) {
                  return 'DA0';
                } else if (value === 20) {
                  return '5M';
                } if (value === 40) {
                  return '20M'
                } else if (value === 60) {
                  return '50M'
                }
                return `${value}M`;
              },
            },
            title: {
              display: true,
              text: 'OverView',
              font: {
                size: 14,
                weight: 'bold',
              },
            },
          },
        },
      },
    };
  },
};
</script>

<style scoped>
.container {
  position: absolute;
  left: 25%;
  top: 150%;
  width: 47%;
  height: 460px;
}

</style>
