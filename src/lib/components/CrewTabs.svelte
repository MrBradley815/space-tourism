<script>
  export let items = []
  export let activeTabValue = 1

  const handleClick = tabValue => () => (activeTabValue = tabValue)
</script>

<div class="crew-tabs">
  {#each items as item}
    {#if activeTabValue == item.value}
      <svelte:component this={item.component} />
    {/if}
  {/each}
  
  <ul>
    {#each items as item}
      <li class="{activeTabValue === item.value ? 'active' : ''}">
        <button on:click={handleClick(item.value)}></button>
      </li>
    {/each}
  </ul>
</div>

<style>
  ul {
    list-style-type: none;
    display: flex;
    gap: 2.4rem;
  }

  button {
    background-color: var(--color-white);
    width: 1.5rem;
    height: 1.5rem;
    border: 0;
    border-radius: 50%;
    outline: none;
    opacity: 0.175;
    cursor: pointer;
    transition: all .2s;
  }

  button:hover {
    opacity: 0.5;
  }

  li.active button {
    opacity: 1;
  }
</style>