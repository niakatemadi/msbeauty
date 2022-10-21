<template>
  <transition :name="slideside">
    <div class="carousel-item" v-show="currentSlide === index">
      <img :src="slideimg" />
    </div>
  </transition>
</template>

<script>
export default {
  name: 'carouselItem',
  props: ['slideimg', 'currentSlide', 'index', 'slideside'],
};
</script>

<style scoped>
.carousel-item {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}
.slide-in-enter-active,
.slide-in-leave-active {
  transition: all 1s ease-in-out;
}
.slide-in-enter {
  transform: translateX(-100%);
}
.slide-in-leave-to {
  transform: translateX(100%);
}
.slide-out-enter-active
{
  transition: all 1s ease-in-out;
}
.slide-out-leave-active {
  transition: all 1s ease-in-out;
}
.slide-out-enter {
  transform: translateX(100%);
}
.slide-out-leave-to {
  transform: translateX(-100%);
  transition: all 1s ease-in-out;
}
</style>
