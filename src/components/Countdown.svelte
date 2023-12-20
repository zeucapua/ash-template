<script lang="ts">
  import { onMount, onDestroy } from "svelte";

  export let duration = 10;
  export let message = "Hello World";
  let countdown_interval : ReturnType<typeof setInterval>;

  onMount(() => {
    countdown_interval = setInterval(() => {
      duration -= 1;
    }, 1000);
  });

  $: if (duration === 0) {
    clearInterval(countdown_interval);

    alert(message);

    // run the HTMX JS API
    // find the element with id 'timer_button', and trigger the 'reset' event
    htmx.trigger("#timer_button", "reset");
  }
  
  onDestroy(() => {
    clearInterval(countdown_interval);
  });
</script>

<p 
  class="bg-orange-100 text-6xl font-bold border-2 border-orange-500 border-dotted px-auto py-2 text-center rounded-lg">
  {duration}
</p>
