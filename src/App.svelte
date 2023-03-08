<script lang="ts">
  import HeaderBar from './components/layout/HeaderBar.svelte';
  import BuildCanvas from './components/layout/BuildCanvas.svelte';
  import ComponentToolbox from './components/layout/ComponentToolbox.svelte';

  const appTitle = "Fast App Builder"
</script>

<main class="w100 h100">
  <HeaderBar title={appTitle}/>
  <ComponentToolbox/>
  <BuildCanvas/>
</main>

<style lang="less">


</style>