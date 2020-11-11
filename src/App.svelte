<script>
  import Tailwindcss from './Tailwindcss.svelte';
  import Table from './Components/Table.svelte';
</script>

<style>
  .table-wrapper {
    width: 90%;
    margin: 0 auto;
    overflow: hidden;
  }
</style>

<Tailwindcss />

<main class="mx-auto">
  <div class="p-10 mx-auto text-5xl text-center text-gray-800">
    <h1>Periodic Table of Svelements</h1>
  </div>
  <div class="table-wrapper">
    <Table />
  </div>
</main>
