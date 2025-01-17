<script setup>
import { reactive } from 'vue'
import img from '../../images/image-devices.png'
import icon1 from '../../images/icon-blacklist.svg'
import icon2 from '../../images/icon-text.svg'
import icon3 from '../../images/icon-preview.svg'
const content = reactive({
	one: {
		icon: icon1,
		alt: 'List icon',
		title: 'Create blacklists',
		text: 'Ensure sensitive information never makes its way to your clipboard by excluding certain sources.',
	},
	two: {
		icon: icon2,
		alt: 'A letter icon',
		title: 'Plain text snippets',
		text: 'Remove unwanted formatting from copied text for a consistent look.',
	},
	three: {
		icon: icon3,
		alt: 'Eye icon',
		title: 'Sneak preview',
		text: 'Quick preview of all snippets on your Clipboard for easy access.',
	},
})
</script>

<template>
	<section class="section">
		<h2 class="secondTitle">Access Clipboard anywhere</h2>
		<p class="desc desc2">
			Whether you’re on the go, or at your computer, you can access all
			your Clipboard snippets in a few simple clicks.
		</p>
		<img :src="img" alt="Tablet and phone" class="img" />
		<h2 class="secondTitle">Supercharge your workflow</h2>
		<p class="desc">We’ve got the tools to boost your productivity.</p>
		<div class="box">
			<div class="textBox" v-for="(value, index) in content" :key="index">
				<div class="imgBox">
					<img :src="value.icon" :alt="value.alt" class="icon" />
				</div>
				<h3 class="thirdTitle">{{ value.title }}</h3>
				<p class="desc descInside">{{ value.text }}</p>
			</div>
		</div>
	</section>
</template>

<style scoped lang="scss">
@include sectionStyles;
@include loopedText;

.icon {
	margin: 1em 0 2.5em 0;
	width: 13%;
}

@media (min-width: 992px) {
	.desc2 {
		margin: 0 auto;
		width: 41.375em;
	}

	.img {
		margin: 0 auto;
		margin-top: 5em;
		width: 87%;
	}

	.secondTitle {
		margin-top: 3em;
		margin-bottom: 0.7em;
	}

	.box {
		display: flex;
		justify-content: center;
		align-items: flex-start;
		column-gap: 1em;
	}

	.descInside {
		max-width: 21.875em;
	}

	.textBox {
		display: grid;
		grid-template-columns: 1fr;
		place-items: center;
	}

	.imgBox {
		height: 3.125em;
		margin-bottom: 2em;
	}

	.icon {
		width: 100%;
		margin-bottom: 5%;
	}
}
</style>
