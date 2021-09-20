<template>
<div>
    <label>Nombre: </label><br>
    <input v-model="nombre">
    <p>Hola {{nombre}}</p>
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