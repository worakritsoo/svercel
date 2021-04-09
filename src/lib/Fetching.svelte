<!-- https://svelte.dev/repl/99c18a89f05d4682baa83cb673135f05?version=3.20.1 -->
<script>
  import { onMount } from 'svelte';
  let data;
  onMount(async () => {
    data = await fetch('https://randomuser.me/api/?results=20').then((x) =>
      x.json()
    );
  });
</script>

<pre>

        {JSON.stringify(data, null, 2)}
</pre>
