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
	border-bottom: 2px solid #269b82;
	box-shadow: 0px 2px 10px #269b82;
	transition: background-color 0.2s;

	&:hover {
		background-color: #5fccb9;
	}

	&:nth-child(2) {
		background-color: $light-blue;
		border-bottom: 3px solid #7d88e2;
		box-shadow: 0px 3px 10px #7d88e2;

		&:hover {
			background-color: #8896ff;
		}
	}
}

@media (min-width: 992px) {
	.btns-box {
		display: flex;
		justify-content: center;
		column-gap: 1.5em;
	}

	.btn {
		margin: 0;
		width: auto;
		font-size: 1.7rem;
		padding: 0.7em 2.2em;
	}
}
</style>
