<script>
  import rocketLg from '$lib/images/technology/image-launch-vehicle-portrait.jpg'
  import rocketSm from '$lib/images/technology/image-launch-vehicle-landscape.jpg'
  import { fade } from 'svelte/transition'
</script>

<div>
  <p class="subheading-sm">THE TERMINOLOGY...</p>
  <h3 in:fade="{{ duration: 750, delay: 200 }}">LAUNCH VEHICLE</h3>
  <p in:fade="{{ duration: 750, delay: 700 }}">A launch vehicle or carrier rocket is a rocket-propelled vehicle used to carry a payload from Earth's surface to space, usually to Earth orbit or beyond. Our WEB-X carrier rocket is the most powerful in operation. Standing 150 meters tall, it's quite an awe-inspiring sight on the launch pad!</p>
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
