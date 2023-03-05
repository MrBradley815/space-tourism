<script>
  import europaImg from '$lib/images/destination/image-europa.webp'
  import { fly, fade } from 'svelte/transition'
</script>

<div class="destination-grid">
  <div>
    <img src="{europaImg}" alt="Europa" class="destination-img" in:fade="{{ duration: 750 }}" />
  </div>
  <div class="destination-info">
    <h2 in:fade="{{ duration: 750, delay: 500 }}">EUROPA</h2>
    <p in:fly="{{ x: 50, duration: 750, delay: 1000 }}" class="destination-description">The smallest of the four Galilean moons orbiting Jupiter, Europa is a winter lover's dream. With an icy surface, it's perfect for a bit of ice skating, curling, hockey, or simple relaxation in your snug wintery cabin.</p>
    <div class="divider"></div>
    <div class="row">
      <div class="col-50" in:fly="{{ y: 50, duration: 750, delay: 1500 }}">
        <p class="subheading-sm">AVG. DISTANCE</p>
        <p class="subheading-lg">628 MIL. KM</p>
      </div>
      <div class="col-50" in:fly="{{ y: 50, duration: 750, delay: 1750 }}">
        <p class="subheading-sm">EST. TRAVEL TIME</p>
        <p class="subheading-lg">3 YEARS</p>
      </div>
    </div>
  </div>
</div>