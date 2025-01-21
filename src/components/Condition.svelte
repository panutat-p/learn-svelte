<script>
	let count = $state(0)

  $effect(() => {
    const id = setInterval(() => {
      count += 1
    }, 1000)

    return () => {
      clearInterval(id)
    }
  })
</script>

<div>
{#if count > 10}
	<p>{count} is greater than 10</p>
{:else if count < 5}
	<p>{count} is less than 5</p>
{:else}
	<p>{count} is between 5 and 10</p>
{/if}

</div>

<style>
  div {
    margin: 20px;
    padding: 2px;
  }
  p {
    color: rgb(255, 255, 255);
    font-family: 'Comic Sans MS', cursive;
    font-size: 50px;
  }
</style>
