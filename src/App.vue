<template>
  <div id="app">
    <Slider />
  </div>
</template>

<script>
import Slider from './components/Slider.vue'

export default {
  name: 'app',
  components: {
    Slider
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body{
  margin:0px;
}
</style>
