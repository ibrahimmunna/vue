<template>
<h1> If-Else Contidion</h1>
<h1 v-if="on">This is the "IF" statement</h1><!--applying if condition to check either it is true or not-->
<h1 v-else>This is the "ELSE" statement</h1><!--appying the else condition-->
<button @click="toggle">Change Here</button><!--call the toggle function while clicking-->
</template>

<script>
export default{
    name:'IfElse',
    data(){
        return{
            on: true
        }
    },
    methods:{
        toggle(){
            this.on =!this.on
        }
    }
}

</script>