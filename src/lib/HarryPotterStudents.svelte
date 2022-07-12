<script>
  async function harryPotterStudents() {
    const res = await fetch(
      "http://hp-api.herokuapp.com/api/characters/students"
    );
    const json = await res.json();

    if (res.ok) {
      return json;
    } else {
      throw new Error(json);
    }
  }

  let promise = harryPotterStudents();
</script>

<h2>Estudiantes de la saga de Harray Potter (promesas)</h2>
{#await promise}
  <p>Esperando resutlado...</p>
{:then students}
  <p>Total Estudiantes: {students.length}</p>
  {#each students as { name, house, image: src }}
    {#if src}
      <h3>{name} ({house})</h3>
      <img {src} width="100" alt={name} />
    {/if}
  {/each}
{:catch error}
  <p style="color:red;">Ocurrio un error: {error}</p>
{/await}
