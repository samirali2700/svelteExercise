<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  function sayHello() {
    dispatch("message", {
      text: "Hello!",
    });
  }
</script>

<p class="title">Events</p>
<button
  on:click={sayHello}
  style="position:absolute; left:15px; top: 105px; width:150px;"
  >Say Hello</button
>
