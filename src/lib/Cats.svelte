<script>
    let cats = [
        {id: 1, name:'Cat 1'},
        {id: 2, name:'Cat 2'},
        {id: 3, name:'Cat 3'},
    ]
</script>

<h2>Listando Gatos con #each </h2>
<ul style="list-style: none;">
    <!-- {#each cats as cat, i}
        <li>{i+1} {cat.name}</li>
    {/each} -->
    {#each cats as {id,name}}
        <li>{id} {name}</li>
    {/each}
</ul>
