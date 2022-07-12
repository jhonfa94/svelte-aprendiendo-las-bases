<script>
  import Cat from "./dynamicComponents/Cat.svelte";
  import Dog from "./dynamicComponents/Dog.svelte";
  import Horse from "./dynamicComponents/Horse.svelte";

  const components = [
    { label: "Gato", cmp: Cat, },
    { label: "Perro", cmp: Dog, },
    { label: "Horse", cmp: Horse, },
  ];

  let componentSelect = components[0];
</script>

<select bind:value={componentSelect.label}>
  {#each components as component}
    <option value={component.label}>{component.label}</option>
  {/each}
</select>

<svelte:component this={componentSelect.cmp} />
