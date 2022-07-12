<script>
    let user = {
        LoggedIn:false
    }

    const toogle = () => user.LoggedIn = !user.LoggedIn
</script>

<h2>Condicional if else</h2>

{#if user.LoggedIn}
    <button on:click="{toogle}">
        Log out
    </button>
{:else}
    <button on:click="{toogle}">
        Log in
    </button>
{/if}