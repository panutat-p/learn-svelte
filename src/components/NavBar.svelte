<script lang="ts">
  let links = $state([
    { name: 'Home', href: '/' },
    { name: 'About', href: '/about' },
  ])
</script>

<nav>
  <ul>
    {#each links as { name, href }}
      <li><a href={href}>{name}</a></li>
    {/each}
  </ul>
</nav>

<style>
  nav {
    background-color: #f8f8f8;
    padding: 1em 2em;
  }
  ul {
    list-style: none;
    display: flex;
    gap: 1em;
  }
  li {
    font-size: 1.2em;
  }
  a {
    text-decoration: none;
    color: #333;
  }
  a:hover {
    color: #ff3e00;
  }
</style>
