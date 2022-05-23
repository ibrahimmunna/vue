<template>
<h1>Form Binding</h1>
<input v-model="text" @click="onInput" placeholder="Type here"/>
<p>You are typing: {{text}}</p>
</template>
<script>
export default{
    name:'FormBinding',
    data(){
        return{
            text:''
        }
    },
    method:{
        onInput(typed){
            this.text = typed.target.value
        }
    }
}
</script>