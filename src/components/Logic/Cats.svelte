<script>
  let cats = [
    { id: "J---aiyznGQ", name: "Keyboard Cat" },
    { id: "z_AbfPXTKms", name: "Maru" },
    { id: "OUtn3pvWmpg", name: "Henri The Existential Cat" },
  ];
</script>

<h1>Famous Cat Videoes</h1>

<div>
  {#each cats as { id, name }, i}
    <a href="https://www.youtube.com/watch?v={id}">
      {i + 1}: {name}
    </a>
  {/each}
</div>

<style>
  div {
    display: flex;
    flex-direction: column;
  }
  a:hover {
    color: #000;
  }
</style>
