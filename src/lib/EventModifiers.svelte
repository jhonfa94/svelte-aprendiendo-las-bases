<script>
  const handleClick = () => {
    alert("Solo se ejecuta la primera vez");
  };
</script>

<h2>Modificadors de enventos (once)</h2>

<button on:click|once={handleClick}> Pulsa, sólo se ejecutara una vez </button>
