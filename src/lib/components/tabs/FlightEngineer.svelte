<script>
  import portrait from '$lib/images/crew/image-anousheh-ansari.webp'
  import { fly } from 'svelte/transition'
</script>

<div class="crew-info">
  <h4 in:fly="{{ x: -100, duration: 750 }}">FLIGHT ENGINEER</h4>
  <h3 in:fly="{{ x: -100, duration: 750, delay: 250 }}">ANOUSHEH ANSARI</h3>
  <p in:fly="{{ x: -100, duration: 750, delay: 500 }}">Anousheh Ansari is an Iranian American engineer and co-founder of Prodea Systems. Ansari was the fourth self-funded space tourist, the first self-funded woman to fly to the ISS, and the first Iranian in space.</p>
  <img src="{portrait}" alt="Victor Glover" in:fly="{{ x: 100, duration: 750, delay: 500 }}" />
</div>

<style>
  img {
    right: 13vw;
  }
</style>