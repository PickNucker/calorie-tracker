<script setup lang="ts">
import Chart from 'chart.js/auto'
import { onMounted } from 'vue';

const data = {
  labels: [
    'Red',
    'Blue',
    'Yellow'
  ],
  datasets: [{
    label: 'My First Dataset',
    data: [300, 50, 100],
    backgroundColor: [
      'rgb(255, 99, 132)',
      'rgb(54, 162, 235)',
      'rgb(255, 205, 86)'
    ],
    hoverOffset: 4
  }]
};

const config = {
  type: 'doughnut',
  data: data,
};

onMounted(() => {
  const myChart = new Chart(
    document.getElementById("chart"),
    config
  )
})

const items = ['Protein', 'Fett']

</script>

<template>
  <v-card variant="tonal" class="d-flex size">
    <canvas id="chart"></canvas>
    <v-card class="mx-auto" max-width="300">
      <v-list :items="items" item-title="name" item-value="id"></v-list>
    </v-card>
  </v-card>
</template>
