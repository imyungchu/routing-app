<script setup>
    import { ref, onBeforeMount } from 'vue';
    import { useRoute } from 'vue-router';
    import cars from '../data.json';

    const dealer = ref('');
    const route = useRoute();

    onBeforeMount(() => {
        const carId = route.params.id;
        const car = cars.find(c => c.id === parseInt(carId));
        if (car) {
            dealer.value = car.dealer;
        }
    })
</script>

<template>
    <div>
        <h1>{{ dealer }}</h1>
    </div>
</template>

