<script>
  let input;

  export function focus() {
    input.focus();
  }
</script>

<h2>Referencias a Componentes</h2>
<input bind:this="{input}" type="text">
