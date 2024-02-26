<script lang="ts">
  import Router from 'svelte-spa-router';
  import Header from './lib/components/header/header.svelte';
  import {default as Index} from './lib/routes/page.svelte';
  import {default as Projects} from './lib/routes/projects/page.svelte';
    import { writable } from 'svelte/store';
    import { onMount, setContext } from 'svelte';

  const routes = {
    '/': Index,
    '/projects': Projects
  }

  let isMobile = writable(window.innerWidth < 768);
  window.addEventListener('resize', () => {
    $isMobile = window.innerWidth < 768;
  });
  setContext('isMobile', isMobile);
</script>

<Header/>
<main>
  <Router {routes}/>
</main>