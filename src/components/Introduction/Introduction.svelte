<script>
  export let name;
  export let src;
  export let htmlString;
</script>

<p class="title">Introduction</p>
<h1>Hello {name}</h1>
<p>{@html htmlString}</p>
<img style="width:200px;" {src} alt="A man Dancing" />

<style>
</style>
