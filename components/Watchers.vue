<template>
<h1>Watchers</h1>
<p> ToDo ID: {{todoID}}</p>
<button @click="todoID++">Fetch Next ToDo</button>
<p v-if="!todoData">Loading . . .</p>
<pre v-else>{{todoData}}</pre>

</template>

<script>
export default{
    name:'WatchersMethod',
    data(){
        return{
            todoID: 1,
            todoData: null
        }
    },
    methods:{
        async fetchData(){
            this.todoData = null
            const res =  await fetch(`https://jsonplaceholder.typicode.com/todos/${this.todoID}`)
            this.todoData =  await res.json()
        }
    },
    mounted(){
        this.fetchData()
    },
    watch:{
        todoID(){
            this.fetchData()
        }
    }
}
</script>