<template>
<h1>LifeCycle Hooks </h1>
<h4>Use the consile panel to use this!</h4>
<input v-model="text"/>
<p>{{text}}</p>  
</template>
<script>
export default{
    name:'LifeCycle',
    data(){
        return{
            text:''
        
        }
             
    },
    beforeCreate(){
        console.log("Before Create")
    },
    created(){
            console.log("Created")
        },
    beforeMount(){
        console.log("Before Mount")
    },
    mounted(){
            console.log("mounted")
        },
        beforeUpdate(){
            console.log("Before Update")
        },
        updated(){
            console.log("Updated")
        },
    unmounted(){
            console.log("unmounted")
        }
}
</script>