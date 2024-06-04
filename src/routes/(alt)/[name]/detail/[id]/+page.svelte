<script>
  import {page} from '$app/stores';
  import Detail from '$lib/detail/Detail.svelte';
</script>
<Detail id={$page.params.name} />

<em>Now click back</em>