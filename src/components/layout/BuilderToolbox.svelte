<script lang="ts">
	import ComponentToolbox from "./BuilderToolbox/ComponentToolbox.svelte";
	import ViewNavigation from "./BuilderToolbox/ViewNavigation.svelte";

</script>

<template>
	<section class="builder-toolbox flex-column h100">
		<ViewNavigation height="20%"/>
		<ComponentToolbox height="80%"/>
	</section>
</template>

<style lang="less">
	.builder-toolbox {
		width: 20%;
	}
</style>