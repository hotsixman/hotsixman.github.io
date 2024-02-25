<script lang="ts">
  import Router from 'svelte-spa-router';
  import Header from './lib/components/header/header.svelte';
  import {default as Index} from './lib/routes/page.svelte';
  import {default as Projects} from './lib/routes/projects/page.svelte';

  const routes = {
    '/': Index,
    '/projects': Projects
  }
</script>

<Header/>
<main>
  <Router {routes}/>
</main>