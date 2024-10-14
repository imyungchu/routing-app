<script setup>
    import { ref, onBeforeMount } from 'vue';
    import { useRoute } from 'vue-router';
    import cars from '../data.json';

    const manufacturer = ref('');
    const route = useRoute();

    onBeforeMount(() => {
        const carId = route.params.id;
        const car = cars.find(c => c.id === parseInt(carId));
        if (car) {
            manufacturer.value = car.manufacturer;
        }
    })
</script>

<template>
    <div>
        <h1>{{ manufacturer }}</h1>
    </div>
</template>

