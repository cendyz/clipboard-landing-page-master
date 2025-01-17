<script setup>
import { ref } from 'vue'
import logo from '../images/logo.svg'
import fbIcon from '../images/icon-facebook.svg'
import twitterIcon from '../images/icon-twitter.svg'
import instagramIcon from '../images/icon-instagram.svg'
const linksData = ref({
	one: {
		text: 'FAQs',
	},
	two: {
		text: 'Contact Us',
	},
	three: {
		text: 'privacy policy',
	},
	four: {
		text: 'press kit',
	},
	five: {
		text: 'install guide',
	},
})
const iconsData = ref({
	one: { icon: fbIcon, alt: 'Facebook logo' },
	two: { icon: twitterIcon, alt: 'Twitter logo' },
	three: { icon: instagramIcon, alt: 'Instagram logo' },
})
</script>

<template>
	<footer class="footer">
		<img :src="logo" alt="Logo company C" class="logo" />
		<div class="linksBox">
			<a
				href="#"
				class="link"
				v-for="(value, index) in linksData"
				:key="index"
				>{{ value.text }}</a
			>
		</div>
		<div class="iconsBox">
			<img
				:src="value.icon"
				:alt="value.atl"
				class="icon"
				v-for="(value, index) in iconsData"
				:key="index" />
		</div>
	</footer>
</template>

<style scoped lang="scss">
.footer {
	padding: 3em;
	background-color: rgb(240, 240, 240);
}

.logo {
	display: block;
	margin: 0 auto 3em auto;
	width: 18%;
}

.linksBox {
	margin-bottom: 2.5em;
	display: grid;
	text-align: center;
	row-gap: 1.5em;
}

.link {
	text-transform: capitalize;
	color: $dark-grayish-blue;
}

.iconsBox {
	display: flex;
	justify-content: center;
	align-items: center;
	column-gap: 2em;
}
</style>
