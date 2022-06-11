<script>
    import image1 from '../Images/banner-inicio-camaras-1.jpg';
    import image2 from '../Images/banner-inicio-cercos-1.jpg';
    import image3 from '../Images/banner-inicio-incendio-1.jpg';
    import image4 from '../Images/banner-inicio-monitoreo-1.jpg';
    let images = [image2, image3, image4]

    import Slider from '../Components/Slider.svelte';

    import empresaImg from '../Images/empresa.jpg'
</script>

<main>
    <Slider firstImage={image1} images={images} />
    <div class="container py-5 px-5 empresa-container">
        <h4>Acerca de Real Security</h4>
        <div class="row">
            <div class="col-12 col-lg-8">
                <p class="text-secondary">
                    Somos una empresa de Ingeniería y Proyectos con más de 20 años de reconocida experiencia en el campo de la Seguridad Electrónica en el Perú.
                    Contamos con personal técnico propio y una filosofía de trabajo avocada siempre a la calidad, lo cual nos ha ayudado en la practica a ofrecer productos y servicios con TOTAL GARANTIA.
                    Iniciamos actividades en agosto de 1998 y hasta la fecha nos hemos desempeñado ininterrumpidamente alcanzando con ello niveles bastante reconocidos de excelencia y pleno conocimiento del campo. A finales del 2019 realizamos un Upgrading de nuestros sistemas de gestión ante la SUNAT como empresa PYME, con lo cual nos vimos obligados en redefinir una nueva fecha de inicio de actividades (Diciembre 2019).
                    Brindamos asesoría y presupuestos tanto en nuevas instalaciones como para sistemas ya existentes.
                    Para mayores informes nos pueden ubicar en nuestras oficinas llamando a los Teléfonos (01) 462-0868 / 981469760 o vía WhatsApp y estaremos gustosos de atenderlos.
                    <br><br>
                    LA GERENCIA
                </p>
            </div>
            <div class="col-12 col-lg-4" style="display: grid; place-items: center">   
                <img src={empresaImg} alt="">
            </div>
        </div>

    </div>
</main>

<style>
    img{
        max-width: 100%;
    }
    .empresa-container{
        background-color: #fff;
    }
</style>