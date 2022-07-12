<script>
    $: user = {
        name: "jfcm",
        email: "jfcmdev@gmail.com"
    }
</script>

<h2>Formulario simple</h2>

<form action="">
    <label for="nombre">Nombre</label>
    <input type="text" name="nombre" id="nombre" bind:value="{user.name}">
    <br>
    <label for="email">Email</label>
    <input type="email" name="email" id="email" bind:value="{user.email}">
    <br>
</form>

<pre>
    {
        JSON.stringify(user)
    }
</pre>