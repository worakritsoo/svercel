<script>
  export let href = '';
  export let title = '';
  export let color = '';
</script>

<a {href} style={`color: ${color}`}>
  {title}
</a>

// Shorthand
<a {href} style={`color: ${color}`}>
  {title}
</a>
