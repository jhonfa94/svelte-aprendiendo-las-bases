<script>
 let age = 7;
</script>

<h2>Condicioal If Else IF</h2>

{#if age >= 18}
    <p>Ya eres mayor de edad</p>
{:else if (age > 10)}
    <p>Eres menor de 10 años</p>
{:else}
    <p>Tienes entre 10 y 17 años</p>
{/if}