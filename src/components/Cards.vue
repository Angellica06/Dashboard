<template>
  <div class="col mt-2">
    <div class="card shadow">
      <h5 class="card-title m-1 p-2">{{ title }}</h5>
      <hr class="my-0 mx-3">
      <div class="card-body" :style="{ height: cardHeight }">
        <graficoBar v-if="chart == 'bar'"></graficoBar>
        <graficoLine v-if="chart == 'line'"></graficoLine>
        <graficoPolar v-if="chart == 'polar'"></graficoPolar>
      </div>
    </div>
  </div>

</template>

<script setup>
import graficoBar from './graficos/graficoBar.vue';
import graficoLine from './graficos/graficoLine.vue';
import graficoPolar from './graficos/graficoPolar.vue';

const props = defineProps(['title', 'chart', 'cardHeight']);
</script>

<style scoped>
.card {
  border-radius: .6rem;
}
.card-body {
  color: #000;
}
</style>