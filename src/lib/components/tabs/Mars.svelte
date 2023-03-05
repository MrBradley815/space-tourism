<script>
  import marsImg from '$lib/images/destination/image-mars.webp'
  import { fly, fade } from 'svelte/transition'
</script>

<div class="destination-grid">
  <div>
    <img src="{marsImg}" alt="Mars" class="destination-img" in:fade="{{ duration: 750 }}" />
  </div>
  <div class="destination-info">
    <h2 in:fade="{{ duration: 750, delay: 500 }}">MARS</h2>
    <p in:fly="{{ x: 50, duration: 750, delay: 1000 }}" class="destination-description">Don't forget to pack your hiking boots. You'll need them to tackle Olympus Mons, the tallest planetary mountain in our solar system. It's two and a half times the size of Everest!</p>
    <div class="divider"></div>
    <div class="row">
      <div class="col-50" in:fly="{{ y: 50, duration: 750, delay: 1500 }}">
        <p class="subheading-sm">AVG. DISTANCE</p>
        <p class="subheading-lg">225 MIL. KM</p>
      </div>
      <div class="col-50" in:fly="{{ y: 50, duration: 750, delay: 1750 }}">
        <p class="subheading-sm">EST. TRAVEL TIME</p>
        <p class="subheading-lg">9 MONTHS</p>
      </div>
    </div>
  </div>
</div>