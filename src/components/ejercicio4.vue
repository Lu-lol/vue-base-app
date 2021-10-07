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
    <div>
        <ul>
            <input type="text" v-model="text">
            <button @click="add()">Agregar</button>
            <li v-for="text in list" v-bind:key="text.id">{{text}}</li>
        </ul>
    </div>
</template>