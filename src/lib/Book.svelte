<script>
    export let title;
    export let author;
    export let isbn;
    export let published;
</script>

<h2>Libro con ...spread operator</h2>
<article>
    <p>Título: {title}</p>
    <p>Author: {author}</p>
    <p>ISBN: {isbn}</p>
    <p>Publicado: {published ? 'Si' : 'No'}</p>
</article>