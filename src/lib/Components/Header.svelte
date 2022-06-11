<script>
    import Logo from '../Images/logo.jpg';
    import Placa from '../Images/placa.jpg'
</script>


<header>
    <div class="container-fluid header-container">
        <div class="container px-2">
            <div class="row py-2 d-none d-lg-flex">
                <div class="col">
                    <a href="/#/">
                        <img src={Logo} alt="" class="logo">
                    </a>
                </div>
                <div class="col d-flex">
                    <div class="d-flex ms-auto text-secondary align-items-center">
                        <img src={Placa} alt="">
                        <small>
                            Luis N. Saénz 549 - Jesús María<br>
                            Tel.(01)462-0868 / 981469760<br>
                            soporte@realsecurityperu.com
                        </small>
                    </div>
                </div>
            </div>
        </div>
    </div> 
</header>

<style>
    .logo{
        max-height: 80px;
    }
    .header-container{
        background-color: var(--header-color);
    }
</style>
