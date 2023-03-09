<script lang="ts">
	export let text: string = undefined;
	export let type: "ghost" | "primary" | "success" | "danger" | "transparent" = "transparent";
	export let icon: string = undefined;

	let className: string = undefined;
	export { className as class };

	export let onClick: (event: MouseEvent) => void = undefined;
</script>

<template>
	<button class={`${className} ${type}`} on:click={onClick}>
		{#if icon}
			<span class="material-icons">{icon}</span>
		{/if}
		{#if text}
			<span>{text}</span>
		{/if}
	</button>
</template>

<style lang="less" scoped>
	button {
		border: none;
		border-radius: 4px;
		background: transparent;

		padding: 0.5em 1em;

		&:hover {
			cursor: pointer;
			filter: saturate(0.7);
		}
	}

	.primary {
		background-color: var(--primary-color);
		color: var(--white);
	}

	.success {
		background-color: var(--success-color);
	}

	.danger {
		background-color: var(--danger-color);
		color: var(--white)
	}

	.ghost {
		background-color: transparent;
		border-color: var(--secondary-color);
		color: var(--secondary-color);

		&:hover {
			color: var(--green4);
		}
	}

	.transparent {
		background-color: transparent;
		color: var(--font-color);
	}

</style>