<script lang="ts">
	import Icon from "./Icon.svelte";


	export let title: string = undefined;
	export let height = "unset";
    export let foldable = false;
    export let onFoldChange: (folded: boolean) => void = () => {};

    let folded = false;

    function toggleFold() {
        if (!foldable) return;

        folded = !folded;
        onFoldChange(folded);
    }
</script>

<section class={`flex-column toolbox w100 ${foldable ? 'foldable' : ''}`} style={`height: ${height};`}>
    {#if title}
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <div class="flex-centered" on:click={toggleFold}>
            <h3>{title}</h3>
            {#if foldable}
                <Icon icon={folded ? "expand_more" : "expand_less"} />
            {/if}
        </div>
    {/if}
    {#if !folded}
        <slot />
    {/if}
</section>

<style lang="less">
    .foldable:hover {
        cursor: pointer;
    }
</style>