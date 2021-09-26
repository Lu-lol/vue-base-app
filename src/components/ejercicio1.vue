<template>
<div>
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
.n, .h{
    text-align: center;
}
</style>