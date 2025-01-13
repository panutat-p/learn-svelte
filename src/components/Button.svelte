<script lang="ts">
  let { color, backgroundColor } = $props()

  let count = $state(0)

  function increment() {
    count += 1
  }
</script>

<div>
  <button onclick={increment} style:color={color} style:background-color={backgroundColor}>
    Clicked {count}
  </button>
</div>

<style>
  div {
    margin: 20px;
    padding: 2px;
  }
  button {
    border: none;
    padding: 10px 20px;
    font-size: 1.5em;
    cursor: pointer;
  }
</style>
