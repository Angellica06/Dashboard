<template>
    <canvas id="myChart" class="w-100"></canvas>
</template>

<script setup>
import Chart from 'chart.js/auto';
import { onMounted } from 'vue';

onMounted(() => {
    const ctx = document.getElementById('myChart')

    const chart = new Chart(ctx, {
        type: 'bar',
        data: {
            labels: ['Janeiro', 'Fevereiro', 'Março', 'Abril', 'Maio', 'Junho'],
            datasets: [{
                label: 'Produto A',
                data: [110, 19, 30, 50, 44, 33],
                backgroundColor: '#c7417b',
                borderColor: '#c7417b',
            },
            {
                label: 'Produto B',
                data: [150, 28, 84, 90, 20, 68],
                backgroundColor: '#23306a',
                borderColor: '#23306a',
            }
            ]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            scales: {
                y: {
                    beginAtZero: true
                }
            },
            plugins: {
                legend: {
                    labels: {
                        boxHeight: 6,
                        usePointStyle: true,
                    },
                }
            }
        }
    }); chart;
})

</script>