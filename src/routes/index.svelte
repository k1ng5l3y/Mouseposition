<script>
import Outer from "./outer.svelte";

  let mp = {x:0, y:0};

  function handleMousechange(event){
    mp.x = event.clientX;
    mp.y = event.clientY;
  }

  function handleMessage(event){
    alert(event.detail.text);
  }
</script>

<style>
  .plain{
    width: 100%;
    height: 100%;
  }
</style>

<div on:mousemove={handleMousechange} class="plain">
  <h1>The position of the mouse is: {mp.x} , { mp.y }</h1>
  <h1>Welcome to SvelteKit</h1>
  <p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
</div>


<Outer on:message={handleMessage}/>