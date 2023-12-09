<script lang="ts">
  let count = 0;

  const increment = () => {
    count += 1;
  };

  const decrement = () => {
    count -= 1;
  };
</script>


<div>
    <p>Count: {count}</p>
    <button on:click={increment}>Increment</button>
    <button on:click={decrement}>Decrement</button>
  </div>