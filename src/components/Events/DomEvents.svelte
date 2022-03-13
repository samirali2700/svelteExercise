<script>
  import ComponentEvent from "./SubDomEvent.svelte";
  let m = { x: 0, y: 0 };

  function handleMouseEvent(e) {
    m.x = e.clientX;
    m.y = e.clientY;
  }
  function handleClick() {
    alert("no more alerts");
  }
</script>

<div
  on:mousemove={handleMouseEvent}
  on:mouseleave={() => (m = { x: 0, y: 0 })}
  style="width:100%; height:100%;"
>
  <p>The Mouse position is: {m.x} x {m.y}</p>
  <button on:click|once={handleClick} style="top: 55px;">Click Me Once</button>
  <ComponentEvent on:message />
</div>

<style>
  p {
    position: absolute;
    top: 15px;
    left: 15px;
  }
  button {
    position: absolute;
    left: 15px;
    width: 150px;
  }
</style>
