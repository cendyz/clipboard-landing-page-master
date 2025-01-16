<script setup>
import logo from '../images/logo.svg'
import patternMobile from '../images/bg-header-mobile.png'
import { reactive } from 'vue'
const btns = reactive({
	one: 'iOS',
	two: 'Mac',
})
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
		<div class="btns-box">
			<button v-for="(value, index) in btns" :key="index" class="btn">
				Download for {{ value }}
			</button>
		</div>
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
}

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
