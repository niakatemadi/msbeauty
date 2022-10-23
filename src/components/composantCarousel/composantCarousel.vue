<template>
  <div class="Carousel">
    <div class="Carousel-inner">
      <carouselItem
        v-for="(slide, index) in slides"
        :key="`item-${index}`"
        :currentSlide="currentSlide"
        :index="index"
        :slideimg="slide"
        :slideside="slideside"
      />
      <slideIndicator :slides="slides" :currentSlide="currentSlide" />
      <carouselControl @next-item="nextItem" @prev-item="prevItem" />
    </div>
  </div>
</template>

<script>
import carouselItem from './carouselItem.vue';
import carouselControl from './carouselControls.vue';
import slideIndicator from './slideIndicator.vue';
export default {
  name: 'composantCarousel',
  components: { carouselItem, carouselControl, slideIndicator },
  data() {
    return {
      currentSlide: 0,
      intervalId: null,
      slideside: null,
    };
  },
  props: {
    slides: {
      type: Array,
      required: true,
    },
  },
  methods: {
    setCurrentSlide(index) {
      this.currentSlide = index;
    },
    prevItem(payload) {
      if (this.currentSlide === 0) {
        this.slideside = payload.side;
        this.currentSlide = 4;
      } else {
        this.slideside = payload.side;
        const index =
          this.currentSlide <= this.slides.length - 1
            ? this.currentSlide - payload.number
            : 0;
        this.currentSlide = index;
      }
    },
    nextItem(payload) {
      console.log('uuuu', payload.side);
      this.slideside = payload.side;
      const index =
        this.currentSlide < this.slides.length - 1 ? this.currentSlide + 1 : 0;
      this.currentSlide = index;
    },
  },
  mounted() {
    this.intervalId = setInterval(() => {
      this.nextItem();
    }, 5000);
  },
  beforeUnmount() {
    clearInterval(this.intervalId);
  },
};
</script>
<style scoped>
.Carousel {
  display: flex;
  justify-content: center;
  background-color: rgb(192, 192, 192);
}
.Carousel-inner {
  position: relative;
  width: 640px;
  height: 426px;
  overflow: hidden;
}
</style>
