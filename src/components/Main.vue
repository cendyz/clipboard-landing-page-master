<script setup>
import FirstSection from './Sections/FirstSection.vue'
import FourthSection from './Sections/FourthSection.vue';
import SecondSection from './Sections/SecondSection.vue';
import ThirdSection from './Sections/ThirdSection.vue';
import Footer from './Footer.vue';
</script>

<template>
	<main class="main wrapper">
		<FirstSection />
		<SecondSection />
        <ThirdSection />
        <FourthSection />
	</main>
    <Footer />
</template>

<style scoped lang="scss">
.main {
	display: grid;
	row-gap: 5em;
	padding: 1.5em;
}
</style>
