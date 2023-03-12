<script>
  import Counter from './lib/Counter.svelte'
</script>

<main>
  <div>
    <img src="/chart.svg" class="logo" alt="Vite Logo" />
  </div>
  <h1>Svelte Charts</h1>

  <div class="card">
    <Counter />
  </div>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
</style>
