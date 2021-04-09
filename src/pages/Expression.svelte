<script>
  let isShowing = true;
  let cat = 'cat';
  let user = { name: 'John Wick' };
  let email = 'professionalkiller@gmail.com';
</script>

<p>2 + 2 = {2 + 2}</p>

<p on:click={() => (isShowing = !isShowing)}>
  {isShowing ? 'NOW YOU SEE ME 👀' : 'NOW YOU DON`T SEE ME 🙈'}
</p>

<p>My e-mail is {email}</p>
<p>{user.name}</p>
<p>{cat + `s`}</p>
<p>{`name ${user.name}`}</p>
