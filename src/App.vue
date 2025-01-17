<script setup>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
</script>
<template>
	<Header />
	<Main />
</template>

<style lang="scss">
@use './sass/reset.scss';

body {
	font-family: 'Bai Jamjuree', serif;
	font-size: 1.6rem;
}

.wrapper {
	width: 100%;
	max-width: 1220px;
	margin: 0 auto;
}
</style>
