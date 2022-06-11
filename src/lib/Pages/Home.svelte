<script>
    import image1 from '../Images/banner-inicio-camaras-1.jpg';
    import image2 from '../Images/banner-inicio-cercos-1.jpg';
    import image3 from '../Images/banner-inicio-incendio-1.jpg';
    import image4 from '../Images/banner-inicio-monitoreo-1.jpg';
    let images = [image2, image3, image4]

    import Slider from '../Components/Slider.svelte';

    import alarmas from '../Images/alarmas1.jpg'
    import camaras from '../Images/camaras1.jpg'
    import monitoreo from '../Images/monitoreo1.jpg'
</script>

<main>
    <Slider firstImage={image1} images={images}/>

    <div class="container bg-white text-secondary pt-4 pb-3">
        <div class="row">
            <div class="col-12 col-md-6 col-lg-4">
              <div class="container-fluid">
                <div class="row">
                  <h4 class="text-uppercase mb-0">Alarmas</h4>
                  <p>Contra robos e incendios</p>
                </div>
                <div class="row">
                  <img class="s-img" src={alarmas} alt="">
                </div>
                <div class="row mt-2">
                  <p>Nuestros Ingenieros diseñarán un plan de seguridad orientado a proteger, de manera estratégica…</p>
                </div>
                <div class="row">
                    <button class="btn read-more">Leer más...➜</button>
                </div>
              </div>
            </div>
            <div class="col-12 col-md-6 col-lg-4">
              <div class="container-fluid">
                <div class="row">
                  <h4 class="text-uppercase mb-0">Camaras</h4>
                  <p>Via internet-WIFI</p>
                </div>
                <div class="row">
                  <img class="s-img" src={camaras} alt="">
                </div>
                <div class="row mt-2">
                  <p>REAL SECURITY suministra e instala equipos profesionales, discretos y confiables, que transmiten vía internet…</p>
                </div>
                <div class="row">
                    <button class="btn read-more">Leer más...➜</button>
                </div>
              </div>
            </div>
            <div class="col-12 col-md-6 offset-md-3 offset-lg-0 col-lg-4">
              <div class="container-fluid">
                <div class="row">
                  <h4 class="text-uppercase mb-0">Monitoreo 24 horas</h4>
                  <p>Central de alarmas y Seguridad</p>
                </div>
                <div class="row">
                  <img class="s-img" src={monitoreo} alt="">
                </div>
                <div class="row mt-2">
                  <p>Un comunicador electrónico avisa ante cualquier evento a nuestras oficinas de <b>MONITOREO…</b></p>
                </div>
                <div class="row pe-2">
                    <button class="btn read-more">Leer más...➜</button>
                </div>
              </div>
            </div>
        </div>
    </div>
</main>

<style>
    .read-more{
        color: #fff;
        max-width: 120px;
        background-color: var(--main-color);
        margin-left: auto;
    }
</style>