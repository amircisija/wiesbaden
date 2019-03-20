<template>
  <div>
    <b-carousel
      id="carousel1"
      style="text-shadow: 1px 1px 2px #333;"
      controls
      indicators
      background="#ababab"
      :interval="40000"
      img-width="1024"
      img-height="480"
      v-model="slide"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <div class="overlay__shadow"></div>
      <!-- Slides with custom text -->
      <b-carousel-slide img-src="~/static/img/slide__1.jpg">
        <h1>Hello world!</h1>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    }
  }
};
</script>
<style lang="scss">
#carousel__wrapper {
  height: 100vh;
  .carousel-inner {
    height: 100vh !important;
  }
}
.carousel-caption {
  top: 50%;
  transform: translateY(-50%);
  bottom: initial;
}
.carousel-item {
  -webkit-transform-style: preserve-3d;
  -moz-transform-style: preserve-3d;
  transform-style: preserve-3d;
}
</style>