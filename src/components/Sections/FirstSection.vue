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
		<p class="desc">
			Clipboard instantly stores any item you copy in the cloud, meaning
			you can access your snippets immediately on all your devices. Our Mac
			and iOS apps will help you organize everything.
		</p>
		<img :src="img" alt="Computer monitor" class="img" />
		<div class="textBox" v-for="(value, index) in content" :key="index">
			<h3 class="thirdTitle">{{ value.title }}</h3>
			<p class="desc">{{ value.text }}</p>
		</div>
	</section>
</template>

<style scoped lang="scss">
@include sectionStyles;
@include loopedText;

</style>
