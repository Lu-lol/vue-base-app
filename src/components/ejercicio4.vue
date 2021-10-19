<script>
export default {
    name: 'App',
    newItemName: '',
    newItemQuantity: '',
    
    lastId: 1,
    data() {
        return {
            list: [],
        }
    },
    methods: {
        add: function() {
            let newItem = {
                id: this.lastId,
                name: this.newItemName,
                quantity: this.newItemQuantity
            }
            this.lastId += 1 
            this.list.push(newItem);
            this.newItemName = ''
        },
        
    },
};
</script>
<template>
    <div class="container">
        <h1>Ejercicio 4/5/6</h1>
        <ul class="dot">
            <input type="text" v-model="newItemName">
            <input type="text" v-model="newItemQuantity">
            <button @click="add()">Agregar</button>
            <li v-for="text in list" v-bind:key="text.id" class="text">{{text.name}} x {{text.quantity}}</li>
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
    .text{
        padding-top: 12px;
    }
</style>