<script>
  import Thing from "../Logic/Thing.svelte";

  function removeItem() {
    temp = temp.slice(1);
  }
  function resetItems() {
    temp = things;
  }

  const things = [
    { id: 1, color: "darkblue" },
    { id: 2, color: "indigo" },
    { id: 3, color: "deeppink" },
    { id: 4, color: "salmon" },
    { id: 5, color: "gold" },
  ];
  let temp = things;
</script>

<p class="title">Keyed each block</p>

<button on:click={removeItem}>Remove First Thing</button>
<button on:click={resetItems}>Reset</button>
<div
  style="display: grid; grid-template-columns: 1fr 1fr; column-gap:25px; min-height:250px;"
>
  <div>
    <h2>Keyed</h2>
    {#each temp as thing (thing.id)}
      <Thing current={thing.color} />
    {/each}
  </div>
  <div>
    <h2>unkeyed</h2>
    {#each temp as thing}
      <Thing current={thing.color} />
    {/each}
  </div>
</div>

<style>
  button {
    width: 250px;
  }
</style>
