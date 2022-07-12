<script>
    let current = 'svelte'
</script>

<button 
   class:selected={current==='svelte'}
   on:click={() => current = 'svelte'}
   >   
    Svelte
</button>
<button 
   class:selected={current==='vue'}
   on:click={() => current = 'vue'}
   >   
    Vue
</button>
<button 
   class:selected={current==='react'}
   on:click={() => current = 'react'}
   >   
    React
</button>

<style>
    button{
        display: block;
        margin:auto;
        padding: 5px;
    }

    .selected{
        background-color: #ff3e00;
        color: white;
    }
</style>