<template>
  <div>
    <ul>
      <li
        v-for="(slide, index) in slides"
        :key="`item-${index}`"
        :class="currentSlide == index ? 'indicatorcolor' : 'nocolor'"
      ></li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'slideIndicator',
  props: ['slides', 'currentSlide'],
};
</script>
<style scoped>
div {
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  align-items: flex-end;
}
ul {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 200px;
  height: 50px;
  list-style: none;
  padding: 0;
}
li {
  background-color: white;
  width: 20px;
  height: 5px;
}
.indicatorcolor {
  background-color: rgba(187, 34, 179,0.7);
}
.nocolor {
  border: 1px solid rgba(187, 34, 179,1);
}
</style>
