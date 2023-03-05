<script>
  import Logo from './Logo.svelte'
  import NavLink from './NavLink.svelte'
</script>

<nav>
  <div class="logo">
    <Logo />
  </div>
  <div class="line"></div>
  <ul class="nav-links">
    <NavLink href="/" title="{{ id: '00', text: 'Home' }}" />
    <NavLink href="/destination" title="{{ id: '01', text: 'Destination' }}" />
    <NavLink href="/crew" title="{{ id: '02', text: 'Crew' }}" />
    <NavLink href="/technology" title="{{ id: '03', text: 'Technology' }}" />
  </ul>
</nav>

<style>
  nav {
    display: flex;
    align-items: center;
    padding-left: 5.5rem;
  }

  .logo {
    margin-right: 3.4rem;
  }

  .line {
    position: relative;
    flex-grow: 1;
    background-color: var(--color-white);
    opacity: 0.25;
    height: 1px;
    max-width: 33vw;
    transform: translateX(3rem);
    z-index: 1;
  }

  .nav-links {
    display: flex;
    align-items: center;
    gap: 4.8rem;
    flex-grow: 1;
    list-style: none;
    background-color: rgba(255 255 255 / 4%);
    padding-left: 8.5vw;
    backdrop-filter: blur(3.5rem);
  }
</style>