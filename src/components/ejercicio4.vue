<script>
export default {
    name: 'App',   
    data() {
        return {
            list: [],
             newItemName: '',
             newItemQuantity: ''
        }
    },
    methods: {
        add: function() {
            let newItem = {
                id: this.uuidv4(),
                name: this.newItemName,
                quantity: this.newItemQuantity
            }
            this.list.push(newItem);
            this.newItemName = '',
            this.newItemQuantity = ''
        },
            deleteItem(itemId){
                this.items = this.items.filter((item) => item.id !== itemId)
            },
        uuidv4() {
                return 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
                var r = Math.random() * 16 | 0, v = c == 'x' ? r : (r & 0x3 | 0x8);
                return v.toString(16);
                });
            },
    },
};
</script>
<template>
    <div class="container">
        <h1>Ejercicio 4/5/6</h1>
        <ul class="dot">
            <input type="text" v-model="newItemName">
            <input type="text" v-model.number="newItemQuantity">
            <button @click="add()" v-if="!newItemName=='' && newItemQuantity!=0 && !isNaN(newItemQuantity)">Agregar</button>
            <li v-for="text in list" v-bind:key="text.id" class="text">{{text.name}} x {{text.quantity}} <button @click="deleteItem(text.id)">X</button></li>
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