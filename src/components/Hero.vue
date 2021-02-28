<template>
  <section class="hero">
    <b-carousel
      id="carousel-1"
      :interval="4000"
      controls
      background="#ababab"
      style="text-shadow: 0px 1px 2px #444;"
    >
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid hero-img"
            src="../assets/images/carousel-1.jpg"
            alt="onepage-carousel-1"
          >
        </template>
        <div class="container">
            <h1>We transform every dream into digital reality</h1>
            <a href="#" class="btn btn-lg btn-primary rounded-pill" title="Discover">Discover</a>
        </div>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid hero-img"
            src="https://picsum.photos/1440/598/?image=26"
            alt="onepage-carousel-2"
          >
        </template>
        <div class="container">
            <h1>Hello world!</h1>
            <a href="#" class="btn btn-lg btn-primary rounded-pill" title="Discover">Discover</a>
        </div>
      </b-carousel-slide>

    </b-carousel>
  </section>
</template>

<script>
  export default {
    
  }
</script>