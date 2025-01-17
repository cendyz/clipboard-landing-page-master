<script setup>
import { ref } from 'vue'
import icon1 from '../../images/logo-google.png'
import icon2 from '../../images/logo-ibm.png'
import icon3 from '../../images/logo-microsoft.png'
import icon4 from '../../images/logo-hp.png'
import icon5 from '../../images/logo-vector-graphics.png'
const icons = ref({
	one: {
		icon: icon1,
		alt: 'Google logo',
	},
	two: {
		icon: icon2,
		alt: 'IBM logo',
	},
	three: {
		icon: icon3,
		alt: 'Microsoft logo',
	},
	four: {
		icon: icon4,
		alt: 'HP logo',
	},
	five: {
		icon: icon5,
		alt: 'Vector graphics logo',
	},
})
</script>

<template>
	<section class="section">
		<img
			:src="value.icon"
			:alt="value.alt"
			v-for="(value, index) in icons"
			:key="index"
			class="img" />
	</section>
</template>

<style scoped lang="scss">
.section {
	display: flex;
	flex-direction: column;
	row-gap: 3em;
}

.img {
	display: block;
	margin: 0 auto;
	width: 35%;
}

@media (min-width: 992px) {
	.section {
		flex-direction: row;
		align-items: center;
		column-gap: 6em;
	}
}
</style>
