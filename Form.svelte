<script>
  let lists = ["banana", "orange"];
  let input = "";

  function handleChange(e) {
    input = e.target.value;
  }

  function addItem() {
    lists.push(input);
    lists = lists;
  }

  function removeItem(i) {
    lists.splice(i, 1);
    lists = lists;
  }
</script>

<style>
</style>

<div>
  <input on:change={handleChange} />
  <button on:click={addItem}>Add</button>
  <ul>
	{#each lists as list, i}
		<li>{list}</li>
    <button on:click={() => removeItem(i)}>x</button>
	{/each}
</ul>
</div>