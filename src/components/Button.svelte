<script lang="ts">
  export let text: string;
  export let handleClick: () => void;
</script>

<button on:click={handleClick}>
  {text}
</button>
