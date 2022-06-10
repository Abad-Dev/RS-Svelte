<script>
  import Router, {location} from 'svelte-spa-router';
  import Home from './lib/Pages/Home.svelte';
  import Empresa from './lib/Pages/Empresa.svelte';
</script>

<Router routes={{
  '/': Home,
  '/about': Empresa,
}}
/>
