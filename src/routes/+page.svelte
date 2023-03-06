<script>
  import '$lib/css/home.css'
  import img from '$lib/images/home/background-home-desktop.jpg'
  import { onMount } from 'svelte'
  import { fade, fly } from 'svelte/transition'

  onMount(() => {
    document.body.style.backgroundImage = `url(${img})`
  })
</script>

<div class="container">
  <div class="home-inner">
    <div>
      <h5 in:fly="{{ y:100, duration: 750 }}">SO, YOU WANT TO TRAVEL TO</h5>
      <h1 in:fly="{{ y:100, duration: 750, delay: 500 }}">SPACE</h1>
      <p in:fly="{{ y:100, duration: 750, delay: 1000 }}">Let's face it; if you want to go to space, you might as well genuinely go to outer space and not hover kind of on the edge of it. Well sit back, and relax because we'll give you a truly out of this world experience!</p>
    </div>
    <a href="/destination" class="explore" in:fade="{{ duration: 500, delay: 2000 }}">EXPLORE</a>
  </div>
</div>
