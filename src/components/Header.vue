<script setup>
import logo from '../images/logo.svg'
import patternMobile from '../images/bg-header-mobile.png'
import patternDesktop from '../images/bg-header-desktop.png'
import Btns from './Btns.vue'
</script>

<template>
	<header class="header wrapper">
		<img :src="logo" alt="Company logo c letter" class="logo" />
		<picture>
			<source :src="patternDesktop" media="(min-width:992px)" />
			<img :src="patternMobile" alt="Wallpaper" class="pattern" />
		</picture>
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
	z-index: -1;
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

@media (min-width: 992px) {
	.logo {
		width: 15%;
	}

	.title {
		font-size: 3.7rem;
	}

	.desc {
		margin: 1em auto 3em auto;
		max-width: 37.75em;
	}
}
</style>
