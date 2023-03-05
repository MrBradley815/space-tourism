<script>
  import titanImg from '$lib/images/destination/image-titan.webp'
  import { fly, fade } from 'svelte/transition'
</script>

<div class="destination-grid">
  <div>
    <img src="{titanImg}" alt="Titan" class="destination-img" in:fade="{{ duration: 750 }}" />
  </div>
  <div class="destination-info">
    <h2 in:fade="{{ duration: 750, delay: 500 }}">TITAN</h2>
    <p in:fly="{{ x: 50, duration: 750, delay: 1000 }}" class="destination-description">The only moon known to have a dense atmosphere other than Earth, Titan is a home away from home (just a few hundred degrees colder!). As a bonus, you get striking views of the Rings of Saturn.</p>
    <div class="divider"></div>
    <div class="row">
      <div class="col-50" in:fly="{{ y: 50, duration: 750, delay: 1500 }}">
        <p class="subheading-sm">AVG. DISTANCE</p>
        <p class="subheading-lg">1.6 BIL. KM</p>
      </div>
      <div class="col-50" in:fly="{{ y: 50, duration: 750, delay: 1750 }}">
        <p class="subheading-sm">EST. TRAVEL TIME</p>
        <p class="subheading-lg">7 YEARS</p>
      </div>
    </div>
  </div>
</div>