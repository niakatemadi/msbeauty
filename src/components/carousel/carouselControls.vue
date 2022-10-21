<template>
  <div class="Bloc_carouselControl">
    <button class="carousel-control left" @click="prevItem"><img src="../../assets/left-arrow2.png"/></button>
    <button class="carousel-control right" @click="nextItem"><img src="../../assets/right-arrow2.png"/></button>
  </div>
</template>

<script>
export default {
  name: 'carouselControl',
  methods: {
    nextItem() {
      this.$emit('next-item', {
        number: 1,
        side: 'slide-in',
      });
    },
    prevItem() {
      this.$emit('prev-item', {
        number: 1,
        side: 'slide-out',
      });
    },
  },
};
</script>

<style>
.Bloc_carouselControl {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.carousel-control {
  height: 50px;
  width: 70px;
  background-color: rgba(187, 34, 179,0);
  outline: none;
  background: transparent;
  border: 1px solid transparent;
  color: white;
}
.carousel-control:hover {
  cursor: pointer;
}
</style>
