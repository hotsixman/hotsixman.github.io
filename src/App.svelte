<script lang="ts">
  import {Router, Route} from 'svelte-routing';
  import Header from './lib/components/header/header.svelte';
  //import {default as Index} from './lib/routes/page.svelte';

  export let url = "";
</script>

<Header/>
<main>
  <!--
  <Router {url}>
      <Route path="/" component={Index}/>
  </Router>
  -->
</main>