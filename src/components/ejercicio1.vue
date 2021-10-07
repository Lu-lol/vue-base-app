<template>
<div class="container">
    <h1>Ejercicio 1</h1>
    <label>Nombre: </label><br>
    <input class="n" v-model="nombre">
    <p class="h" >Hola {{nombre}}</p>
</div>
</template>
<script>
export default {
    name: 'Main',
    data: function(){
    return {
            nombre: ""
        }
    }
}
</script>

<style>
    .container{
        text-align:center; 
        margin: 0;
        padding: 0;
        display: inline-block;
        overflow: hidden;
        width: 100%;
    }
</style>