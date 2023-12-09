<script lang="ts">
  import Button from "../components/Button.svelte";
  import Counter from "../components/Counter.svelte";
  import { onMount } from "svelte";
  import { writable } from "svelte/store";
  import TodoItem from "../components/TodoItem.svelte";

  // btn click functions
  const handleClick = () => {
    alert("Button clicked!");
  };

  //   todo item functions
  let newTodo = "";
  let todos = writable<string[]>([]);

  const addTodo = () => {
    if (newTodo.trim() != "") {
      todos.update((currentTodo) => [...currentTodo, newTodo]);
      newTodo = "";
    }
  };
</script>

<h1>Welcome to Your Svelte TypeScript App!</h1>

<Counter />

<Button text="Click me" {handleClick} />


<h1>Todo Lists</h1>
{#each $todos as todo (todo)}
  <TodoItem todo={todo} />
{/each}

