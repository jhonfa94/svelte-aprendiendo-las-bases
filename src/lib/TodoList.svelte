<script>
  let todos = [
    { done: true, text: "todo 1" },
    { done: false, text: "todo 2" },
    { done: false, text: "todo 3" },
  ];

  function add() {
    todos = todos.concat({ done: false, text: "" });
  }

  function clear() {
    todos = todos.filter((t) => !t.done);
  }

  $: remaining = todos.filter((t) => !t.done).length;
</script>

<h2>Lista de tareas</h2>

{#each todos as { done, text: value }}
  <div class:done>
    <input type="checkbox" bind:checked={done} />

    <input type="text" placeholder="¿Qué neceistas hacer hoy?"
        bind:value
    >
  </div>
{/each}

<p>{remaining} tareas pendientes</p>
<pre>
    {JSON.stringify(todos)}
</pre>

<button on:click="{add}">
    Añadir tarea
</button>

<button on:click="{clear}">
    Eliminar completadas
</button>

<style>
  .done {
    opacity: 0.4;
  }
</style>
