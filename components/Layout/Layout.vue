<template>
	<u-transition :mode="props.mode" :show="props.show">
		<slot></slot>
	</u-transition>
</template>

<script setup>
	const props = defineProps({
		mode: {
			type: String,
			default: 'fade',
		},
		show: {
			type: Boolean,
			default: false,
		},
	});
</script>

<style></style>