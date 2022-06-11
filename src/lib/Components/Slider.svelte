<script>
    export let firstImage;
    export let images = [];
</script>


<div class="container p-0">
    <div id="carouselExampleControls" class="carousel slide carousel-fade" data-bs-ride="carousel">
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src={firstImage} class="d-block w-100 m-0" alt="">
          </div>
          {#each images as image}
          <div class="carousel-item">
            <img src={image} class="d-block w-100" alt="">
          </div>
          {/each}
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
    </div>
</div>
<style>
    .container{
        border-top: 5px solid #000;   
    }

    img{
        max-width: 100% !important;
        height: 100%;
    }
</style>