<script setup>
	import carsData from './data.json'
	import { ref } from 'vue'
	
	const cars = ref( carsData )
</script>

<template>
	<main>
		<h1>Our Cars</h1>
		<div>
			<div v-for='car in cars' :key='car.id'>
				<h1>{{ car.make }}</h1>
				<p>${{ car.price }}</p>
			</div>
		</div>
	</main>
</template>

<style scoped>
</style>