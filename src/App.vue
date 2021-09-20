<template>
  <div id="app">
    <ejercicio-1 />
    <ejercicio-2 />
  </div>
</template>

<script>
import Ejercicio1 from './components/ejercicio1.vue'
import Ejercicio2 from './components/ejercicio2.vue'

export default {
  components: {
    Ejercicio1,
    Ejercicio2,
  },
  name: 'App',
}
</script>

<style>

</style>