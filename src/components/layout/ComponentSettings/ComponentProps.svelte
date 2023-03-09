<script lang="ts">
	import Toolbox from '../../fabUiComponents/Toolbox.svelte';

	export let height = "unset";
</script>

<template>
	<Toolbox title="Props" {height} foldable>
		<p>Props Selection</p>
	</Toolbox>
</template>

<style lang="less"></style>