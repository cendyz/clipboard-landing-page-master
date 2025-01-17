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
		<div class="wrapper">
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

@media (min-width: 992px) {
	.wrapper {
		display: flex;
		align-items: center;
		justify-content: start;
		column-gap: 8em;
	}

	.logo {
		width: 7%;
		margin: 0;
	}

	.linksBox {
		margin: 0;
		display: flex;
		flex-direction: column;
		flex-wrap: wrap;
		column-gap: 5em;
		height: 4.25em;
	}

	.link {
		text-align: left;
		transition: color 0.2s;

		&:hover {
			color: $strong-cyan;
		}
	}

	.icon {
		cursor: pointer;
		filter: 0;
		transition: filter 0.2s;

		&:hover {
			filter: invert(60%) sepia(26%) saturate(1109%) hue-rotate(121deg)
				brightness(97%) contrast(87%);
		}
	}

	.iconsBox {
		margin-left: auto;
	}
}
</style>
