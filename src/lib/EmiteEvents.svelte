<script>
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  function emitHello() {
    dispatch("message",{
        text:"Hola desde un evento",
    })
  }
</script>

<h2>Eventos de hijos a padres</h2>
<div>
    <button on:click={emitHello}>
        Pulsa para emitir un evento
    </button>
</div>
