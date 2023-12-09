<script lang="ts">
  export let todo: string;
</script>

<div>
  <h3>entered todo</h3>
  <input id="todo" type="checkbox" placeholder="Type Your Todo" />
  <label for="todo">{todo}</label>
</div>