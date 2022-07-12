<script>
  let html = `<p>Escribre algo de <b>texto</b></p>`;
</script>

<h2>Content editable con html binding</h2>
<div contenteditable="true"
    bind:innerHTML="{html}"
>

</div>

{@html html}

<style>
    [contenteditable]{
        padding: 0.5em;
        border: 1px solid black;
        border-radius:5px;
    }
</style>
