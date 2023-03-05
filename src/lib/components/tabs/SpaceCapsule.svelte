<script>
  import capsuleLg from '$lib/images/technology/image-space-capsule-portrait.jpg'
  import capsuleSm from '$lib/images/technology/image-space-capsule-landscape.jpg'
  import { fade } from 'svelte/transition'
</script>

<div>
  <p class="subheading-sm">THE TERMINOLOGY...</p>
  <h3 in:fade="{{ duration: 750, delay: 200 }}">SPACE CAPSULE</h3>
  <p in:fade="{{ duration: 750, delay: 700 }}">A space capsule is an often-crewed spacecraft that uses a blunt-body reentry capsule to reenter the Earth's atmosphere without wings. Our capsule is where you'll spend your time during the flight. It includes a space gym, cinema, and plenty of other activities to keep you entertained.</p>
  <picture in:fade="{{ duration: 750, delay: 1200 }}">
    <source media="(min-width: 1000px)" srcset="{capsuleLg}">
    <img src="{capsuleSm}" alt="Rocket" />
  </picture>
</div>

<style>
  div {
    position: relative;
    width: 100%;
    max-width: 47rem;
  }
  img {
    position: absolute;
    top: 0;
    right: 0;
    transform: translate(125%, -21%);
  }
</style>
