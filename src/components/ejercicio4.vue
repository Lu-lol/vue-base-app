<script>
export default {
    data() {
        return {
            list: []
        }
    },
    methods: {
        add: function() {
            this.list.push(this.text);
        },
    },
}
</script>
<template>
    <div class="container">
        <h1>Ejercicio 4</h1>
        <ul class="dot">
            <input type="text" v-model="text">
            <button @click="add()">Agregar</button>
            <li v-for="text in list" v-bind:key="text.id">{{text}}</li>
            <p v-if="list.length==0">No hay nada</p>
        </ul>
    </div>
</template>

<style>
    .dot{
        list-style-type: none;
        padding: 0;
    }
    .container{
        text-align:center; 
        margin: 0;
        padding: 0;
        display: inline-block;
        overflow: hidden;
        width: 100%;
    }
</style>