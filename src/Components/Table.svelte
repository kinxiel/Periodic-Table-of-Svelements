<script>
  import { elements } from '../Data/PeriodicTableJSON.json';
  import Element from './Element.svelte';
</script>

<style>
  .table {
    display: grid;
    grid-template-columns: repeat(18, auto) 1fr;
    gap: 0.1vw;
  }
</style>

<div>
  <div class="table text-gray-900">
    {#each elements as element, i}
      <Element
        atomicNumber={element.number}
        style="grid-column: {element.xpos}; grid-row: {element.ypos}" />
    {:else}{null}{/each}
  </div>
</div>
