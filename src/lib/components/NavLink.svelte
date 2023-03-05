<script>
  import { page } from '$app/stores'
  export let href
  export let title
</script>

<li class="nav-link" class:active="{$page.route.id == href}" ><a {href}><span>{title.id}</span>{title.text}</a></li>

<style>
  .nav-link {
    position: relative;
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 1.6rem;
    letter-spacing: 2.7px;
    text-transform: uppercase;
    color: var(--color-white);
    padding-top: 3.9rem;
    padding-bottom: 3.9rem;
  }

  .nav-link.active::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: var(--color-white);
    height: 3px;
  }

  .nav-link a::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(255 255 255 / 50%);
    height: 3px;
    opacity: 0;
    transition: all .2s;
  }

  .nav-link a:hover::after {
    opacity: 1;
  }

  .nav-link span {
    font-weight: 700;
    margin-right: 1.1rem;
  }
</style>