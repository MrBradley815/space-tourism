<script>
  export let items = []
  export let activeTabValue = 1

  const handleClick = tabValue => () => (activeTabValue = tabValue)
</script>

<div class="technology-tabs">
  <ul>
    {#each items as item}
      <li class="{activeTabValue === item.value ? 'active' : ''}">
        <button on:click={handleClick(item.value)}>{item.value}</button>
      </li>
    {/each}
  </ul>
  
  {#each items as item}
    {#if activeTabValue == item.value}
      <svelte:component this={item.component} />
    {/if}
  {/each}
</div>

<style>
  ul {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 3.2rem;
    margin-right: 8rem;
  }

  li.active button {
    color: var(--color-black);
    background-color: var(--color-white);
  }
</style>
