<script lang="ts">
  import HeaderBar from './components/layout/HeaderBar.svelte';
  import BuildCanvas from './components/layout/BuildCanvas.svelte';
  import ComponentToolbox from './components/layout/BuilderToolbox/ComponentToolbox.svelte';
	import ComponentSettings from './components/layout/ComponentSettings.svelte';
	import BuilderToolbox from './components/layout/BuilderToolbox.svelte';

  const appTitle = "Fast App Builder"
</script>

<main class="w100 h100">
  <HeaderBar title={appTitle}/>
  <div class="builder-content flex-row">
    <BuilderToolbox/>
    <BuildCanvas/>
    <ComponentSettings />

  </div>
</main>

<style lang="less">

  main {
    background-color: var(--bg-color);
    color: var(--text-color);
    font-family: sans-serif;
  }
.builder-content {
  height: calc(100% - 4em);
}

</style>