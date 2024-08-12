<template>
	<font-awesome-icon v-if="isMounted" v-bind="$attrs" />
</template>

<script setup>
import { onMounted, ref } from 'vue';

const isMounted = ref(false);
onMounted(() => {
	isMounted.value = true;
});
</script>
