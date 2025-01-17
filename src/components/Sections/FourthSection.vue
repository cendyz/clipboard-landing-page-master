<script setup>
import Btns from '../Btns.vue'
</script>

<template>
	<section class="section">
		<h2 class="title">Clipboard for iOS and Mac OS</h2>
		<p class="desc">
			Available for free on the App Store. Download for Mac or iOS, sync
			with iCloud and you’re ready to start adding to your clipboard.
		</p>
		<Btns />
	</section>
</template>

<style scoped lang="scss">
@include sectionStyles;

.section {
	margin-bottom: 10em;
}

.title {
	margin-top: 5em;
	color: $dark-grayish-blue;
	padding: 0 1em;
}

.desc {
	margin-bottom: 4em;
}
</style>
