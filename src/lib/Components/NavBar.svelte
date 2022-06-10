<script>
    import { location } from 'svelte-spa-router';
    import navLogo from '../Images/navlogo.jpg'
    let routes = [
        {url: '/#/about', label: 'La empresa'},
        {url: '/#/security', label: 'Seguridad Electronica'},
        {url: '/#/central', label: 'Central de Alarmas'},
        {url: '/#/protection', label: 'Proteccion electrica'},
        {url: '/#/contact', label: 'Contactenos'}
    ];
</script>



<nav class="navbar navbar-expand-lg nav-container navbar-light">
    <div class="container-fluid">
        <a class="d-lg-none" href="/#/">
            <img src={navLogo} alt="">
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mx-auto d-flex justify-content-around container ">
            {#each routes as route}
            <li class="nav-item">
                <a href={route.url} class="nav-link">{route.label}</a>
            </li>
            {/each}
        </ul>
        </div>
    </div>
  </nav>

<style>
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
    }
</style>