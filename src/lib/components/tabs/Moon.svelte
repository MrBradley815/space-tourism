<script>
  import moonImg from '$lib/images/destination/image-moon.webp'
  import { fly, fade } from 'svelte/transition'
</script>

<div class="destination-grid">
  <div>
    <img src="{moonImg}" alt="Moon" class="destination-img" in:fade="{{ duration: 750 }}" />
  </div>
  <div class="destination-info">
    <h2 in:fade="{{ duration: 750, delay: 500 }}">MOON</h2>
    <p in:fly="{{ x: 50, duration: 750, delay: 1000 }}" class="destination-description">See our planet as you've never seen it before. A perfect relaxing trip away to help regain perspective and come back refreshed. While you're there, take in some history by visiting the Luna 2 and Apollo 11 landing sites.</p>
    <div class="divider"></div>
    <div class="row">
      <div class="col-50" in:fly="{{ y: 50, duration: 750, delay: 1500 }}">
        <p class="subheading-sm">AVG. DISTANCE</p>
        <p class="subheading-lg">384,400 km</p>
      </div>
      <div class="col-50" in:fly="{{ y: 50, duration: 750, delay: 1750 }}">
        <p class="subheading-sm">EST. TRAVEL TIME</p>
        <p class="subheading-lg">3 DAYS</p>
      </div>
    </div>
  </div>
</div>