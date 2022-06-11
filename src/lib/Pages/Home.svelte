<script>
    import image1 from '../Images/banner-inicio-camaras-1.jpg';
    import image2 from '../Images/banner-inicio-cercos-1.jpg';
    import image3 from '../Images/banner-inicio-incendio-1.jpg';
    import image4 from '../Images/banner-inicio-monitoreo-1.jpg';
    let images = [image2, image3, image4]

    import Slider from '../Components/Slider.svelte';

    import home1 from '../Images/home1.jpg'
    import home2 from '../Images/home2.jpg'
    import home3 from '../Images/home3.jpg'

    let infos = [
      {
        title: 'Alarmas',
        desc: 'Contra robos e incendios',
        img: home1,
        text: 'Nuestros Ingenieros diseñarán un plan de seguridad orientado a proteger, de manera estratégica…',
        readMoreUrl: '/#/security'
      },
      {
        title: 'Camaras',
        desc: 'Via Internet-WIFI',
        img: home2,
        text: 'REAL SECURITY suministra e instala equipos profesionales, discretos y confiables, que transmiten vía internet…',
        readMoreUrl: '/#/security'
      },
      {
        title: 'Monitoreo 24 Horas',
        desc: 'Central de alarmas y seguridad',
        img: home3,
        text: 'Un comunicador electrónico avisa ante cualquier evento a nuestras oficinas de MONITOREO…',
        readMoreUrl: '/#/security',
      }
    ]
</script>

<main>
    <Slider firstImage={image1} images={images}/>

    <div class="container bg-white text-secondary pt-4 pb-3">
        <div class="row">
            {#each infos as info}
            <div class="col-12 col-md-6 col-lg-4 mt-3 mx-auto">
              <div class="container-fluid">
                <div class="row">
                  <h4 class="text-uppercase mb-0">{info.title}</h4>
                  <p>{info.desc}</p>
                </div>
                <div class="row">
                  <img src={info.img} alt="">
                </div>
                <div class="row mt-2">
                  <p>{info.text}</p>
                </div>
                <div class="row">
                    <a href={info.readMoreUrl} class="btn read-more">Leer más...➜</a>
                </div>
              </div>
            </div>
            {/each}
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