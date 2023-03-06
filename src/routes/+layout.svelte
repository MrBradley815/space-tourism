<script context="module">
  export const load = async ({ url }) => ({ props: { url } });
</script>

<script>
  import '$lib/css/main.css'
  import PageTransition from '$lib/components/PageTransition.svelte'
  import Navbar from '$lib/components/Navbar.svelte'
  import { onMount } from 'svelte'
  import crewBg from '$lib/images/crew/background-crew-desktop.jpg'
  import destinationBg from '$lib/images/destination/background-destination-desktop.jpg'
  import homeBg from '$lib/images/home/background-home-desktop.jpg'
  import technologyBg from '$lib/images/technology/background-technology-desktop.jpg'

  export let url

  let ready = false

  onMount(() => ready = true)
</script>

<svelte:head>
	<link rel="preload" href="{crewBg}" as="image" />
	<link rel="preload" href="{destinationBg}" as="image" />
	<link rel="preload" href="{homeBg}" as="image" />
	<link rel="preload" href="{technologyBg}" as="image" />
</svelte:head>

<PageTransition {url}>
  <Navbar />
  
  {#if ready}
    <slot></slot>
  {/if}
</PageTransition>
