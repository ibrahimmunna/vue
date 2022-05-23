<template>
<h1>Emit Event</h1>
</template>
<script>
export default{
    name:'EmitEvent',
    emits:['response'],
    created(){
        this.$emit('response', "Emit Activated")
    }
}
</script>