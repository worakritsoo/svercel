<!-- App.svelte -->
<script>
  import MyInput from './components/MyInput.svelte';
  import Widget from './components/Widget.svelte';
  import Fetching from './lib/Fetching.svelte';
  import FuzzySearch from './pages/FuzzySearch.svelte';

  export let name;
  let value;
  const title = 'App';

  // Search for items that include "Man" and "Old",
  // OR end with "Artist"
</script>

<header>{title}</header>

<Widget textValue="I'm a svelte component" />

<p>
  <!-- Shorthand -->
  <MyInput bind:value />
  {value}
</p>

<FuzzySearch bind:value />
