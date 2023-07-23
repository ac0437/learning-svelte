<!-- @format -->
<!-- @format -->
<script>
  // @ts-nocheck

  let count = 0;
  const src = 'https://svelte.dev/svelte-logo-horizontal.svg';

  function increment() {
    count++;
  }

  function decrement() {
    count--;
  }
</script>

<nav>
  <img {src} alt="Svelte-logo" />
  <span>Counter</span>
</nav>
<section>
  <div class="count-container">
    <span>{count}</span>
  </div>
  <button on:click={increment}>Increment</button>
  <button on:click={decrement}>Decrement</button>
</section>

<style>
  nav {
    display: flex;
    align-items: center;
  }
  img {
    width: 200px;
  }
  span {
    font-size: 40px;
  }
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .count-container {
    text-align: center;
  }
  section button {
    width: 100px;
    padding: 4px 8px;
  }
  section button {
    margin-top: 8px;
  }
</style>
