<template>
	<div class="row g-3">
		<div v-for="(item, index) in items" :key="index" :class="colClass">
			<!-- <div v-for="(item, index) in items" :key="index" class="col-6"> -->
			<slot :item="item" :index="index"></slot>
		</div>
	</div>
</template>

<script setup>
const props = defineProps({
	items: {
		type: Array,
		required: true,
	},
	colClass: {
		type: String,
		default: 'col-4',
	},
});
console.log('props.items=' + props.items);
console.log('props.colClass=' + props.colClass);
</script>

<style lang="scss" scoped></style>
