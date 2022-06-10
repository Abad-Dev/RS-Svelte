<script>
  import Router from 'svelte-spa-router';
  import Home from './lib/Pages/Home.svelte';
  import Empresa from './lib/Pages/Empresa.svelte';

  import Header from './lib/Components/Header.svelte';
  import NavBar from './lib/Components/NavBar.svelte';
  import Footer from './lib/Components/Footer.svelte';
</script>

<main class="app-container">
  <Header />
  <NavBar />

  <Router routes={{
    '/': Home,
    '/about': Empresa,
  }}
  />  

  <Footer />
</main>

<style>
  :global(:root){
    --header-color: #FFF;
    --main-color: #ffbe00;
    --dark-color: #333333;
  }
  :global(body){
    background: url('./lib/Images/fondo1-1.jpg');
    border-top: 20px solid var(--dark-color);
  }
  :global(img){
    max-width: 65%;
    height: auto;
  }

  :global(#app){
    min-height: 100vh;
  }
  :global(body){
    min-height: 100vh;
  }
  .app-container{
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
</style>