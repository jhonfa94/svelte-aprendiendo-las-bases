<script>
    const elements = ["h1", "h2", "h3", "h4", "h5", "h6", "p"];
    let element = elements[0];
</script>

<select bind:value={element}>
    {#each elements as e}
        <option value={e}>{e}</option>
    {/each}
</select>

<svelte:element this={element}>Etiqueta seleccionada: {element}</svelte:element>
