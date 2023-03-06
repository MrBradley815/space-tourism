<script context="module">
  export const load = async ({ url }) => ({ props: { url } });
</script>

<script>
  import '$lib/css/main.css'
  import PageTransition from '$lib/components/PageTransition.svelte'
  import Navbar from '$lib/components/Navbar.svelte'
  import { onMount } from 'svelte'

  export let url

  let ready = false

  onMount(() => ready = true)
</script>

{#if ready}
  <PageTransition {url}>
    <Navbar />

    <slot></slot>
  </PageTransition>
{/if}
