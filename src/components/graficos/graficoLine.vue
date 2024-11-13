<template>
    <canvas id="Chart" class="w-100"></canvas>
</template>

<script setup>
import Chart from 'chart.js/auto';
import { onMounted } from 'vue';

onMounted(() => {
    const ctx = document.getElementById('Chart');

    const chart = new Chart(ctx, {
        type: 'line',
        data: {
            labels: ['Janeiro', 'Fevereiro', 'Março', 'Abril', 'Maio', 'Junho'],
            datasets: [{
                label: 'Engajamento(páginas visitadas)',
                data: [200, 142, 383, 287, 150, 300],
                backgroundColor: '#ae76ef',
                borderColor: '#ae76ef',
            },
            {
                label: 'Vendas',
                data: [126, 95, 294, 290, 100, 300],
                backgroundColor: '#49cad9',
                borderColor: '#49cad9',
            }
            ]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            scales: {
                y: {
                    beginAtZero: true,
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