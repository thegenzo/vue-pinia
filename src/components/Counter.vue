<template>
	<div>
		<h4>{{ count }}</h4>
		<h5>Double count: {{ doubleCount }}</h5>
		<button @click="increment">Increment</button>
		<button @click="decrement">Decrement</button>
	</div>
</template>

<script setup>
import { storeToRefs } from 'pinia';
import { useCounterStore } from '../store/counter' 
const store = useCounterStore()

const { count, doubleCount } = storeToRefs(store)
const { increment, decrement } = store
</script>

<style scoped>
	button {
		margin: 10px
	}
</style>