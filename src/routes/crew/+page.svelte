<script>
  import '$lib/css/crew.css'
  import img from '$lib/images/crew/background-crew-desktop.jpg'
  import CrewTabs from '$lib/components/CrewTabs.svelte'
  import Commander from '$lib/components/tabs/Commander.svelte'
  import MissionSpecialist from '$lib/components/tabs/MissionSpecialist.svelte'
  import Pilot from '$lib/components/tabs/Pilot.svelte'
  import FlightEngineer from '$lib/components/tabs/FlightEngineer.svelte'
  import { onMount } from 'svelte'
  import { fly } from 'svelte/transition'

  let items = [
    {
      value: 1,
      component: Commander
    },
    {
      value: 2,
      component: MissionSpecialist
    },
    {
      value: 3,
      component: Pilot
    },
    {
      value: 4,
      component: FlightEngineer
    }
  ]

  onMount(() => {
    document.body.style.backgroundImage = `url(${img})`
  })
</script>

<div class="container">
  <div class="crew">
    <h5 in:fly="{{ y:100, duration: 750 }}"><span>02</span>MEET YOUR CREW</h5>
    <CrewTabs {items} />
  </div>
</div>