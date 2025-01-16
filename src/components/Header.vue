<script setup>
import logo from '../images/logo.svg'
import patternMobile from '../images/bg-header-mobile.png'
import Btns from './Btns.vue'
</script>

<template>
	<header class="header">
		<img :src="logo" alt="Company logo c letter" class="logo" />
		<img :src="patternMobile" alt="Wallpaper" class="pattern" />
		<img src="" alt="" class="pattern" />
		<h1 class="title">A history of everything you copy</h1>
		<p class="desc">
			Clipboard allows you to track and organize everything you copy.
			Instantly access your clipboard on all your devices.
		</p>
		<Btns />
	</header>
</template>

<style scoped lang="scss">
.header {
	padding: 8em 1.5em;
	text-align: center;
}

.logo {
	margin: 0 auto;
	margin-bottom: 3.5em;
	display: block;
	width: 30%;
}

.pattern {
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
}

.title {
	color: $dark-grayish-blue;
}

.desc {
	margin: 1em 0 3em 0;
	color: $grayish-blue;
	font-size: 1.7rem;
    line-height: 1.5;
}
</style>
