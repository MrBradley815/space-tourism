<script>
  import rocketLg from '$lib/images/technology/image-spaceport-portrait.jpg'
  import rocketSm from '$lib/images/technology/image-spaceport-landscape.jpg'
  import { fade } from 'svelte/transition'
</script>

<div>
  <p class="subheading-sm">THE TERMINOLOGY...</p>
  <h3 in:fade="{{ duration: 750, delay: 200 }}">SPACEPORT</h3>
  <p in:fade="{{ duration: 750, delay: 700 }}">A spaceport or cosmodrome is a site for launching (or receiving) spacecraft, by analogy to the seaport for ships or airport for aircraft. Based in the famous Cape Canaveral, our spaceport is ideally situated to take advantage of the Earth's rotation for launch.</p>
  <picture in:fade="{{ duration: 750, delay: 1200 }}">
    <source media="(min-width: 1000px)" srcset="{rocketLg}">
    <img src="{rocketSm}" alt="Rocket" />
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
