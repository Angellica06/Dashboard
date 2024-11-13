<template>
    <div class="col mt-2">
        <div class="card shadow" :style="{ backgroundColor: background }">
            <div class="card-body text-light">
                <h5 class="d-flex justify-content-center">{{ title }}</h5>
                <h4 class="d-flex justify-content-evenly">{{ description }}
                    <i :class="`bi ${iconClass}`"></i>
                </h4>
            </div>
        </div>
    </div>
</template>

<script setup>
const props = defineProps(['title', 'description', 'background', 'iconClass']);
</script>

<style scoped>
.card {
    border-radius: .6rem;
}

.card i {
    font-size: 1.6rem;
    color: #fff;
}
</style>