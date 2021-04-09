<script>
  const string = 'Svelte';
</script>

{#each string as character}
  <div>
    {character}
  </div>
{/each}
