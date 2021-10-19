<template>
    <section class="container">
        <h1>Ejercicio 2/3</h1>
        <input class="num1" type="text" v-model="num1"> <br>
        <input class="num2" type="text" v-model="num2"> <br>
        <select v-model="operand" class="op"> 
            <option value="+"> + </option>
            <option value="-"> - </option>
            <option value="*"> * </option>
            <option value="/"> / </option>
        </select>
        <button @click="calc">calcular</button>
        <h2 v-if="err != ''">{{err}}</h2>
        <h2 class="result">{{results}}</h2>
    </section>
</template>
<script>
export default {
    name: "ejercicio2",
    data: function(){
        return{
            num1:0,
            num2:0,
            operand:"0",
            results: "-",
            err: ""
        };
    }, 
    methods: {
        calc(){
            if(isNaN(this.num1) || isNaN(this.num2)){
                this.err = "No es un numero";
            } else {
                switch(this.operand){
                case"+":
                    this.err = "";
                    this.results = parseInt(this.num1) + parseInt(this.num2);
                    break;
                case"-":
                    this.err = "";
                    this.results = parseInt(this.num1) - parseInt(this.num2);
                    break;
                case"*":
                    this.err = "";
                    this.results = parseInt(this.num1) * parseInt(this.num2);
                    break;
                case"/":
                    this.err = "";
                    this.results = parseInt(this.num1) / parseInt(this.num2);
                    break;
                }
            }
            }
        },
    };
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
    .op {
        margin-right: 10px;
    }
</style>