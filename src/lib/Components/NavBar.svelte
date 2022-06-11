<script>
    import { location, replace } from 'svelte-spa-router';
    import navLogo from '../Images/logo-nav.jpg'
    let routes = [
        {url: '/#/about', label: 'La empresa'},
        {url: '/#/security', label: 'Seguridad Electronica'},
        {url: '/#/central', label: 'Central de Alarmas'},
        {url: '/#/protection', label: 'Proteccion electrica'},
        {url: '/#/contact', label: 'Contactenos'}
    ];

    let navBar;
    let linksContainer;

    const hideNavBar = () => {
        navBar.classList.add('collapsed')
        linksContainer.classList.remove('show')
    }
</script>



<nav class="navbar navbar-expand-lg nav-container navbar-light" bind:this={navBar}>
    <div class="container-fluid">
        <img src={navLogo} alt="" style="cursor: pointer;" class="d-flex d-lg-none logo" on:click={() => {replace('/'); hideNavBar()}}>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent" bind:this={linksContainer}>
            <ul class="navbar-nav mx-auto d-flex justify-content-around container ">
                {#each routes as route}
                <li class="nav-item">
                    <a 
                        href={route.url} 
                        class={`nav-link ${'/#' + $location === route.url ? 'nav-active' : ''}`}
                        on:click={hideNavBar}
                    >
                        {route.label}
                    </a>
                </li>
                {/each}
            </ul>
        </div>
    </div>
  </nav>

<style>
    .logo{
        max-height: 80px;
    }
    .nav-link{
        font-size: 14px;
        color: #000 !important;
        transition-duration: .4s;
    }
    .nav-link:hover{
        color: #fff !important;
    }
    .nav-container{
        background-color: var(--main-color);
    }
    .nav-active{
        text-decoration: underline #000;
    }
    @media (max-width: 991px) {
        .nav-container {
            background-color: var(--header-color);
        }
        .nav-link{
            color: #000 !important;
        }
        .nav-link:hover{
            color: var(--main-color) !important;
        }
        .nav-active{
            color: var(--main-color);
        }
    }
</style>
