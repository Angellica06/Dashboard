<template>
    <canvas id="myChart2" class="w-100"></canvas>
</template>

<script setup>
import Chart from 'chart.js/auto';
import { onMounted } from 'vue';

onMounted(() => {
    const ctx = document.getElementById('myChart2');

    const chart = new Chart(ctx, {
        type: 'doughnut',
        data: {
            labels: ['Produto A', 'Produto B'],
            datasets: [{
                backgroundColor: ['#c7417b', '#23306a'],
                data: [184, 300]
            }
            ],
            hoverOffset: 4
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    labels: {
                        boxHeight: 8,
                        usePointStyle: true,
                    },
                }
            }
        }
    }); chart;
})
</script>
