<script>

</script>

<article class="widget">
    <h2>
        <slot name="title">
            <span>Título</span>
        </slot>
    </h2>

    <div class="content">
        <slot name="content">
            <span>Contenido</span>
        </slot>
    </div>

    <div class="footer">
        <slot name="footer">
            <span>Footer</span>
        </slot>
    </div>

</article>





<style>
    .widget {
        margin: auto;
        width: 300px;
        border:1px solid black;
        border-radius: 2px;
        box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
        padding:1em;
    }
</style>