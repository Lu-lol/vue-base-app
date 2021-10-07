<template>
  <div id="app">
    <ejercicio-1 />
    <ejercicio-2 />
    <ejercicio-4/>
  </div>
</template>

<script>
import Ejercicio1 from './components/ejercicio1.vue'
import Ejercicio2 from './components/Ejercicio2.vue'
import Ejercicio4 from './components/ejercicio4.vue'


export default {
  components: {
    Ejercicio1,
    Ejercicio2,
    Ejercicio4,
  },
  name: 'App',
}
</script>

<style>
  h1{
    font-size: 31px;
  }
</style>