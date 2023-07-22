<!-- @format -->
<!-- @format -->
<script>
  // @ts-nocheck

  let count = 0;

  function increment() {
    count++;
    console.log(count);
  }

  function decrement() {
    count--;
    console.log(count);
  }
</script>

<button on:click={increment}>Increment</button>
<button on:click={decrement}>Decrement</button>
<span>{count}</span>

<style>
</style>
