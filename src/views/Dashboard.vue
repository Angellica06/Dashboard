<template>
    <div class="row mb-2">
        <div>
            <NavBar></NavBar>
        </div>  
        <div class="row m-auto">
            <div class="d-flex ms-1 justify-content-center flex-wrap">
                <CardTotal class="col-12 col-lg me-2" :iconClass="'bi-people-fill'" :title="'Adoção'" :description="'2,2 mil'" :background="'#5887ed'"></CardTotal>
                <CardTotal class="col-12 col-lg me-2" :iconClass="'bi-heart-fill'" :title="'Engajamento'" :description="'1,6 mil'" :background="'#a05ced'"></CardTotal>
                <CardTotal class="col-12 col-lg me-2" :iconClass="'bi-shield-lock-fill'" :title="'Retenção'" :description="'215,0 mil'" :background="'#192665'"></CardTotal>
                <CardTotal class="col-12 col-lg me-2" :iconClass="'bi-award-fill'" :title="'Taxa de Sucesso'" :description="'4,8'" :background="'#f19527'"></CardTotal>
            </div>
            <div class="d-flex flex-wrap">
                <Cards class="col-12 col-lg-7" :title="'Engajamento e Vendas'" :chart="'line'" :cardHeight="'350px'"></Cards>
                <Cards class="col-12 col-lg ms-lg-2" :title="'Satisfação do Cliente'" :chart="'polar'" :cardHeight="'350px'"></Cards>
            </div>
            <Cards class="col-12 col-lg" :title="'Vendas'" :chart="'bar'" :cardHeight="'350px'"></Cards>
        </div>
    </div>
</template>

<script setup>
import NavBar from '@/components/NavBar.vue'
import Cards from '@/components/Cards.vue';
import CardTotal from '@/components/CardTotal.vue';
</script>

<style scoped>
.content {
    margin: 0 .4rem;
}
</style>
