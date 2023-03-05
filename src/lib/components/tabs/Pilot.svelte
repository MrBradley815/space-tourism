<script>
  import portrait from '$lib/images/crew/image-victor-glover.webp'
  import { fly } from 'svelte/transition'
</script>

<div class="crew-info">
  <h4 in:fly="{{ x: -100, duration: 750 }}">PILOT</h4>
  <h3 in:fly="{{ x: -100, duration: 750, delay: 250 }}">VICTOR GLOVER</h3>
  <p in:fly="{{ x: -100, duration: 750, delay: 500 }}">Pilot on the first operational flight of the SpaceX Crew Dragon to the International Space Station. Glover is a commander in the U.S. Navy where he pilots an F/A-18.He was a crew member of Expedition 64, and served as a station systems flight engineer. </p>
  <img src="{portrait}" alt="Victor Glover" in:fly="{{ x: 100, duration: 750, delay: 500 }}" />
</div>

<style>
  img {
    right: 17vw;
  }
</style>