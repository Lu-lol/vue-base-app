<template>
  <div id="app">
    <h2 class="ej">Ejercicio 1</h2>
    <ejercicio-1 />
    <h2 class="ej">Ejercicio 2, 3</h2>
    <ejercicio-2 />
  </div>
</template>

<script>
import Ejercicio1 from './components/ejercicio1.vue'
import Ejercicio2 from './components/Ejercicio2.vue'


export default {
  components: {
    Ejercicio1,
    Ejercicio2,
  },
  name: 'App',
}
</script>

<style>
.ej {
  text-align: center;
}
</style>