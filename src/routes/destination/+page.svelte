<script>
  import '$lib/css/destination.css'
  import DestinationTabs from '$lib/components/DestinationTabs.svelte'
  import Moon from '$lib/components/tabs/Moon.svelte'
  import Mars from '$lib/components/tabs/Mars.svelte'
  import Europa from '$lib/components/tabs/Europa.svelte'
  import Titan from '$lib/components/tabs/Titan.svelte'
  import img from '$lib/images/destination/background-destination-desktop.jpg'
  import { onMount } from 'svelte'
  import { fly } from 'svelte/transition'

  let items = [
    {
      value: 1,
      label: 'MOON',
      component: Moon
    },
    {
      value: 2,
      label: 'MARS',
      component: Mars
    },
    {
      value: 3,
      label: 'EUROPA',
      component: Europa
    },
    {
      value: 4,
      label: 'TITAN',
      component: Titan
    }
  ]

  onMount(() => {
    document.body.style.backgroundImage = `url(${img})`
  })
</script>

<div class="container">
  <div class="destination">
    <h5 in:fly="{{ y:100, duration: 750 }}"><span>01</span>PICK YOUR DESTINATION</h5>
    <DestinationTabs {items} />
  </div>
</div>