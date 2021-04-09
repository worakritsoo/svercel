<script>
  import { onMount } from 'svelte';
  import Fuse from 'fuse.js';
  let value;
  onMount(async () => {
    const data = await fetch(
      'https://randomuser.me/api/?results=20'
    ).then((x) => x.json());
  });

  const options = {
    // isCaseSensitive: false,
    // includeScore: false,
    // shouldSort: true,
    // includeMatches: false,
    // findAllMatches: false,
    // minMatchCharLength: 1,
    // location: 0,
    includeScore: true,
     threshold: 0.6,
    distance: 100,
    // useExtendedSearch: false,
    // ignoreLocation: false,
    // ignoreFieldNorm: false,
    useExtendedSearch: true,
    keys: ['title', 'author.firstName'],
  };
  const list = [
    {
      title: "Old Man's War",
      author: 'John Scalzi',
    },
    {
      title: 'The Lock Artist',
      author: 'Steve',
    },
    {
      title: 'Artist for Life',
      author: 'Michelangelo',
    },
  ];

  const fuse = new Fuse(list, options);

  // Change the pattern

  let data;
  const handleInput = (e) => {
    let results = fuse.search(`${value}`);
    data = results.map((result) => result.item);
    console.log(data,Fuse.);
  };
</script>

<input bind:value on:input={handleInput} />
<pre>
    {JSON.stringify({data}, null, 2)}

</pre>

<!-- markup (zero or more items) goes here -->
<style>
  /* your styles go here */
</style>
