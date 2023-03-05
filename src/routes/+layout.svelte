<script context="module">
  export const load = async ({ url }) => ({ props: { url } });
</script>

<script>
  import '$lib/css/main.css'
  import PageTransition from '$lib/components/PageTransition.svelte'
  import Navbar from '$lib/components/Navbar.svelte'

  export let url
</script>

<PageTransition {url}>
  <Navbar />

  <slot></slot>
</PageTransition>
