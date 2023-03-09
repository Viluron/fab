<script>
	import Toolbox from '../fabUiComponents/Toolbox.svelte';
	import ComponentEvents from "./ComponentSettings/ComponentEvents.svelte";
	import ComponentProps from "./ComponentSettings/ComponentProps.svelte";


</script>


<template>
	<section class="component-settings flex-column">
		<Toolbox title="Settings" >
			<ComponentProps />
			<ComponentEvents />
		</Toolbox>

	</section>
</template>

<style lang="less">
.component-settings {
	width: 20%;
	background: navy;
}
</style>