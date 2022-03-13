<script>
  let count = 0;

  $: doubled = count * 2;
  $: quadrupled = doubled * 2;

  const handleClick = () => {
    count = count + 1;
  };
  const resetClick = () => {
    count = 0;
  };

  $: if (count > 10) {
    alert(`count is dangerously high!`);
  }
</script>

<p class="title">Reactivity</p>

<div class="reactive">
  <div>
    <button on:click={handleClick}>
      Clicked {count}
      {count === 1 ? "time" : "times"}
    </button>
  </div>
  <div>
    <p>{count} * 2 = {doubled}</p>
    <p>{doubled} * 2 = {quadrupled}</p>
  </div>
  <div>
    <button on:click={resetClick}> Reset Click </button>
  </div>
</div>

<style>
  .reactive {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .reactive > div {
    display: flex;
    position: relative;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    width: 30%;
  }
  button {
    margin: 0;
    width: 100%;
    border: 1px solid rgb(66, 66, 66);
  }
</style>
