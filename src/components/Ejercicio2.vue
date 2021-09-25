<template>
    <section>
        <input type="text" v-model="num1">
        <select v-model="operand"> 
            <option value="+"> + </option>
            <option value="-"> - </option>
            <option value="*"> * </option>
            <option value="/"> / </option>
        </select>
        <input type="text" v-model="num2">
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
            switch(this.operand){
                case"+":
                if(isNaN(this.num1) || isNaN(this.num2)){
                    this.err = "No es un numero";
                } else {
                    this.err = "";
                    this.results = parseInt(this.num1) + parseInt(this.num2);
                }
                break;
                case"-":
                if(isNaN(this.num1) || isNaN(this.num2)){
                    this.err = "No es un numero";
                } else {
                    this.err = "";
                    this.results = parseInt(this.num1) - parseInt(this.num2);
                }
                break;
                case"*":
                if(isNaN(this.num1) || isNaN(this.num2)){
                    this.err = "No es un numero";
                } else {
                    this.err = "";
                    this.results = parseInt(this.num1) * parseInt(this.num2);
                }
                break;
                case"/":
                if(isNaN(this.num1) || isNaN(this.num2)){
                    this.err = "No es un numero";
                } else {
                    this.err = "";
                    this.results = parseInt(this.num1) / parseInt(this.num2);
                }
            }
        },
    },
};
</script>
<style>
.result {
    text-align: center;
}
</style>