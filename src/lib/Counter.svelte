<script lang="ts">
  let count: number = $state(0)
  const increment = () => {
    count += 1
  }
</script>

<button onclick={increment}>
  count is {count}
</button>

<style>
  button {
    border-radius: 8px;
    border: 1px solid transparent;
    padding: 0.6em 1.2em;
    font-size: 2em;
    font-weight: 500;
    font-family: inherit;
    cursor: pointer;
  }
  button:hover {
    border-color: #646cff;
  }
</style>
