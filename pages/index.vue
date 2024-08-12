<template>
	<div>
		<h1>Counter: {{ counter }}</h1>
		<button @click="increment">Increment</button>
	</div>
	<h1>Test FontAwesome</h1>
	<MyFA :icon="['fas', 'coffee']" />
</template>

<script setup lang="ts">
import { useCounterStore } from '@/stores/counter';

const store = useCounterStore();
const counter = computed(() => store.count);
const increment = () => store.increment();
const isMounted = ref(false);

onMounted(() => {
	isMounted.value = true;
});
</script>
