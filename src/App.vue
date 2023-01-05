<template>
  <AnimasjonZoom hallo="Hello world"/>
  <AnimasjonZoom hallo="Dette er nummer 2"/>
</template>


<script>
import AnimasjonZoom from './components/AnimasjonZoom.vue'

export default {
  name: 'App',
  components: {
    AnimasjonZoom
  }
}
</script>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
