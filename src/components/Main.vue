<script setup>
import FirstSection from './Sections/FirstSection.vue'
import SecondSection from './Sections/SecondSection.vue'
</script>

<template>
	<main class="main">
		<FirstSection />
		<SecondSection />
	</main>
</template>

<style scoped lang="scss">
.main {
	display: grid;
	row-gap: 5em;
	padding: 1.5em;
}
</style>
