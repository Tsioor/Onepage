<template>
  <section class="hero">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="0"
      controls
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >

      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=54">
        <h1>We transform every dream into digital reality</h1>
        <a href="#" class="btn btn-primary" title="Discover">Discover</a>
      </b-carousel-slide>
      <b-carousel-slide img-src="https://picsum.photos/1024/480/?image=56">
        <h1>Hello world!</h1>
        <a href="#" class="btn btn-primary" title="Discover">Discover</a>
      </b-carousel-slide>

    </b-carousel>

    <p class="mt-4">
      Slide #: {{ slide }}<br>
      Sliding: {{ sliding }}
    </p>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart() {
        this.sliding = true
      },
      onSlideEnd() {
        this.sliding = false
      }
    }
  }
</script>

<style lang="scss" scoped>
    
</style>