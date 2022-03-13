<script>
  import Cats from "./Cats.svelte";
  let user = { loggedIn: false };
  export let x = 7;

  function toggleLogin() {
    user.loggedIn = !user.loggedIn;
  }
</script>

<p class="title">Logic</p>

{#if user.loggedIn}
  <button on:click={toggleLogin}> Log In </button>
{:else}
  <button on:click={toggleLogin}> Log Out </button>
{/if}

{#if x > 10}
  <p>{x} is greater than 10</p>
{:else if x < 5}
  <p>{x} is less than 5</p>
{:else}
  <p>{x} is between 5 and 10</p>
{/if}

<Cats />

<style>
  button {
    width: 150px;
  }
</style>
