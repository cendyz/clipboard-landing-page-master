<script setup>
import { reactive } from 'vue'
import img from '../../images/image-computer.png'
const content = reactive({
	one: {
		title: 'Quick Search',
		text: 'Easily search your snippets by content, category, web address, application, and more.',
	},
	two: {
		title: 'iCloud Sync',
		text: 'Instantly saves and syncs snippets across all your devices.',
	},
	three: {
		title: 'Complete History',
		text: 'Retrieve any snippets from the first moment you started using the app.',
	},
})
</script>

<template>
	<section class="section">
		<h2 class="secondTitle">Keep track of your snippets</h2>
		<p class="desc desc--top">
			Clipboard instantly stores any item you copy in the cloud, meaning
			you can access your snippets immediately on all your devices. Our Mac
			and iOS apps will help you organize everything.
		</p>
		<div class="box">
			<img :src="img" alt="Computer monitor" class="img" />
			<div class="contentBoxes">
				<div
					class="textBox"
					v-for="(value, index) in content"
					:key="index">
					<h3 class="thirdTitle insideTitle">{{ value.title }}</h3>
					<p class="desc second-desc">{{ value.text }}</p>
				</div>
			</div>
		</div>
	</section>
</template>

<style scoped lang="scss">
@include sectionStyles;
@include loopedText;

@media (min-width: 992px) {
	.desc {
		&--top {
			margin: 0 auto;
			width: 42em;
		}
	}
	.box {
		margin-top: 2em;
		display: grid;
		grid-template-columns: 0.5fr 0.5fr;
		grid-template-rows: auto;
		place-items: center;
	}

	.contentBoxes {
		align-self: center;
	}

	.textBox {
		margin: auto 0;
		width: 21.875em;
	}

	.insideTitle,
	.second-desc {
		text-align: left;
	}

	.second-desc {
		padding: 0;
	}

	.img {
		margin: 3em 0 3em -7em;
		width: 120%;
	}

	@media (min-width: 1440px) {
		.img {
			margin-left: -13em;
			width: 140%;
		}
	}
}
</style>
