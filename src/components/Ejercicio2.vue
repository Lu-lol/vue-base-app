<template>
    <section>
        <input class="num1" type="text" v-model="num1">
        <select v-model="operand" > 
            <option value="+"> + </option>
            <option value="-"> - </option>
            <option value="*"> * </option>
            <option value="/"> / </option>
        </select>
        <input class="num2" type="text" v-model="num2">
        <button @click="calc">calcular</button>
        <h1 v-if="err != ''">{{err}}</h1>
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
            results: "results",
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
.result, .num1, .num2 {
    text-align: center;
}
</style>