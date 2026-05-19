<template>
	<div>
		<h2>보간법</h2>
		<p>{{ message }}</p>
		<p v-once>{{ message }}</p>
		<button v-on:click="message = message + '!'">Click!</button>
		<hr />
		<h2>v-html</h2>
		<p>{{ rawHtml }}</p>
		<p v-html="rawHtml"></p>
		<hr />
		<h2>속성 바인딩</h2>
		<div v-bind:title="dynamicTitle">마우스를 올려보세요</div>
	</div>
</template>

<script>
import { ref } from 'vue';

export default {
	setup() {
		const message = ref("안녕하세요!");
		const rawHtml = ref("<strong>안녕하세요</strong>");
		
		const dynamicTitle = ref("안녕하세요!!!");

		return {
			message,
			rawHtml,
			dynamicTitle
		};
	},
};
</script>

<style lang="scss" scoped></style>
