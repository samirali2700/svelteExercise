<script>
  import Introduction from "./components/Introduction/Introduction.svelte";
  import Reactivity from "./components/Reactivity/Reactivity.svelte";
  import Props from "./components/Props/Props.svelte";
  import Logic from "./components/Logic/Logic.svelte";
  import Things from "./components/Logic/Things.svelte";
  import DomEvents from "./components/Events/DomEvents.svelte";

  const introduction = {
    name: "World",
    src: "https://svelte.dev/tutorial/image.gif",
    htmlString: `Here's are som <strong>html</strong`,
  };

  let xValue = 25;

  function handleMessage(event) {
    alert(event.detail.text);
  }
</script>

<main>
  <div>
    <Introduction {...introduction} />
  </div>
  <div>
    <Reactivity />
  </div>
  <div>
    <Props answer={42} />
  </div>
  <div>
    <Logic x={xValue} />
  </div>

  <div>
    <Things />
  </div>
  <div style="width:100%; height:250px; padding:0;">
    <DomEvents on:message={handleMessage} />
  </div>
</main>

<style>
  div {
    max-width: 750px;
    margin: 50px auto;
    box-shadow: 2px 2px 5px rgba(255, 255, 255, 0.5);
    background-color: #fff;
    border-radius: 10px;
    padding: 35px;
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
