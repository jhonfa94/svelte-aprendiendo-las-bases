<script>
  import { count } from "../stores/counter.js";
  import {onDestroy} from "svelte"

  let countValue;

  const unsubscribe  = count.subscribe(value =>{
    countValue = value
  })

  function increment() {
    count.update((n) => n + 1);
  }

  function decrement() {
    count.update((n) => n - 1);
  }

  function reset() {
    count.set(0);
  }

  onDestroy(unsubscribe)

</script>

<h2>Contador con Store</h2>

<button on:click={increment}> +</button>
<!-- <b>{$count}</b> -->
<b>{countValue}</b>
<button on:click={decrement}> - </button>
<button on:click={reset}> Restablecer contador</button>
