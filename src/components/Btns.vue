<script setup>
import { reactive } from 'vue'
const btns = reactive({
	one: 'iOS',
	two: 'Mac',
})
</script>

<template>
	<div class="btns-box">
		<button v-for="(value, index) in btns" :key="index" class="btn">
			Download for {{ value }}
		</button>
	</div>
</template>

<style scoped lang="scss">
.btns-box {
	display: grid;
	row-gap: 1.5em;
}

.btn {
	display: block;
	margin: 0 auto;
	width: 100%;
	font-size: 1.6rem;
	color: white;
	padding: 0.7em 0;
	background-color: $strong-cyan;
	border-radius: 1.5em;
	border-bottom: 3px solid hsl(171, 67%, 24%);

	&:nth-child(2) {
		background-color: $light-blue;
		border-bottom: 3px solid hsl(233, 46%, 27%);
	}
}
</style>
