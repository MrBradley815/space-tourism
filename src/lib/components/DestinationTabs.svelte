<script>
  export let items = []
  export let activeTabValue = 1

  const handleClick = tabValue => () => (activeTabValue = tabValue)
</script>

<ul>
  {#each items as item}
    <li class="{activeTabValue === item.value ? 'active' : ''}">
      <button on:click={handleClick(item.value)}>{item.label}</button>
    </li>
  {/each}
</ul>

{#each items as item}
  {#if activeTabValue == item.value}
    <svelte:component this={item.component} />
  {/if}
{/each}

<style>
  ul {
    display: flex;
    gap: 3.5rem;
    list-style: none;
    max-width: 44.6rem;
    margin-left: auto;
  }

  button {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 1.6rem;
    letter-spacing: 2.7px;
    color: var(--color-blue);
    background-color: transparent;
    padding-bottom: 1.2rem;
    border: 0;
    border-bottom: 3px solid transparent;
    outline: none;
    cursor: pointer;
    transition: all .2s;
  }

  button:hover {
    border-color: rgba(255 255 255 / 50%);
  }

  li.active button {
    color: var(--color-white);
    border-color: var(--color-white);
  }
</style>