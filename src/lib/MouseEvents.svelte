<script>
  let p = { x: 0, y: 0 };

  function handleMouseMovements(e) {
    p.x = e.clientX;
    p.y = e.clientY;
  }
</script>

<h2>Movimiento del mouse</h2>
<div on:mousemove={handleMouseMovements} id="divPosition">
  La posición del mouse es: <br>
   x: {p.x} <br>
   y: {p.y}
</div>

<style>
    #divPosition{
        width:100%;
        height:100px;
        border:1px solid black;
    }
</style>
