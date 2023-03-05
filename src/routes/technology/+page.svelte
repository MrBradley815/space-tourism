<script>
  import '$lib/css/technology.css'
  import img from '$lib/images/technology/background-technology-desktop.jpg'
  import { onMount } from 'svelte'
  import { fly } from 'svelte/transition'
  import LaunchVehicle from '$lib/components/tabs/LaunchVehicle.svelte'
  import Spaceport from '$lib/components/tabs/Spaceport.svelte'
  import SpaceCapsule from '$lib/components/tabs/SpaceCapsule.svelte'
  import TechnologyTabs from '$lib/components/TechnologyTabs.svelte'

  let items = [
    {
      value: 1,
      component: LaunchVehicle
    },
    {
      value: 2,
      component: Spaceport
    },
    {
      value: 3,
      component: SpaceCapsule
    }
  ]

  onMount(() => {
    document.body.style.backgroundImage = `url(${img})`
  })
</script>

<div class="container">
  <div class="technology">
    <h5 in:fly="{{ y:100, duration: 750 }}"><span>03</span>SPACE LAUNCH 101</h5>
    <TechnologyTabs {items} />
  </div>
</div>