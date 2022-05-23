<template>
    <h1>Event Listener</h1>
    <button @click="increment">Increment Button {{count}}</button>
    <button @click="decrement">Increment Button {{negativeCount}}</button>
</template>
<script>
export default{
    name:'EventListener',
    data(){
        return{
            count: 0,
            negativeCount: 100
        }
    },
    methods:{
            increment(){
                this.count++
            },
            decrement(){
                this.negativeCount--
            }

    }
}
</script>