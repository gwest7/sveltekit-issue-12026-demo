<script>
	import { slide } from 'svelte/transition';
  export let id;

  $: prom = new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve(id)
    }, 100)
  });

</script>

{#await prom}
  ...
{:then val} 
  THIS LINE IS NOT CLEANED UP
  <h1 transition:slide|global>{val}</h1>
{/await}