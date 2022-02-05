<script>
  // this import the component for creating a new event listener 
  import {createEventDispatcher} from 'svelte';
  
  // this line creates a new event dispatcher 
  const dispatch = createEventDispatcher();

  // this function is called when button below is called 
  function sayhello(){
    dispatch( 'message', { text: 'Hello' });
  }
</script>


<button on:click={sayhello}>
  click me now
</button>