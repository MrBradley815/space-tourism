<script>
  import portrait from '$lib/images/crew/image-mark-shuttleworth.webp'
  import { fly } from 'svelte/transition'
</script>

<div class="crew-info">
  <h4 in:fly="{{ x: -100, duration: 750 }}">MISSION SPECIALIST</h4>
  <h3 in:fly="{{ x: -100, duration: 750, delay: 250 }}">MARK SHUTTLEWORTH</h3>
  <p in:fly="{{ x: -100, duration: 750, delay: 500 }}">Mark Richard Shuttleworth is the founder and CEO of Canonical, the company behind the Linux-based Ubuntu operating system. Shuttleworth became the first South African to travel to space as a space tourist.</p>
  <img src="{portrait}" alt="Victor Glover" in:fly="{{ x: 100, duration: 750, delay: 500 }}" />
</div>

<style>
  img {
    right: 16vw;
  }
</style>