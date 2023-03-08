<script lang="ts">
	import Button from "../fabUiComponents/Button.svelte";


	export let title: string;

</script>

<template>
	<div class="header-bar w100 flex">
		<section class="flex-centered w25 flex-justify-start">
			<Button icon="home" />
		</section>
		<section class="w50 flex-centered">
			<h1>{title}</h1>
		</section>
		<section class="flex-centered w25 flex-justify-end"></section>

	</div>
</template>

<style lang="less">
</style>