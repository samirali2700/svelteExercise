<script>
  import SubProps from "./SubProps.svelte";

  export let answer = "Mystery";

  const pkg = {
    name: "svelte",
    version: 3,
    speed: "blazing",
    website: "https://svelte.dev",
  };
</script>

<p class="title">Props</p>
<p>The answer is {answer}</p>
<SubProps {...pkg} />
