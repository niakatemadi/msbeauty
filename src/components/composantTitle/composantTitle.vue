<template>
  <div >
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style scoped>
h1{
  color:rgba(187, 34, 179,1);
  font-family: 'Playfair Display', serif;
  text-align: center;
}
</style>
