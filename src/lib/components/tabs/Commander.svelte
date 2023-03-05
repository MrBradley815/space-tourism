<script>
  import portrait from '$lib/images/crew/image-douglas-hurley.webp'
  import { fly } from 'svelte/transition'
</script>

<div class="crew-info">
  <h4 in:fly="{{ x: -100, duration: 750 }}">COMMANDER</h4>
  <h3 in:fly="{{ x: -100, duration: 750, delay: 250 }}">DOUGLAS HURLEY</h3>
  <p in:fly="{{ x: -100, duration: 750, delay: 500 }}">Douglas Gerald Hurley is an American engineer, former Marine Corps pilot and former NASA astronaut. He launched into space for the third time as commander of Crew Dragon Demo-2.</p>
  <img src="{portrait}" alt="Douglas Hurley" in:fly="{{ x: 100, duration: 750, delay: 500 }}" />
</div>

<style>
  img {
    right: 14vw;
  }
</style>