<template>
<h1> List Rendering</h1>

<input v-model="text" placeholder="Type here"/>
<button @click="addTodo">  Add </button>
<ol>
    <li v-for="todo in todoList" :key="todo.id">{{todo.text}}<button @click="removeTodo(todo)">Remove</button></li>
</ol>
</template>
<script>
let id = 0
export default{
    name:'ListRender',
    data(){
        return{
            text:'',
            todoList:[
                {id: id++, text: 'Wake Up  '}
            ]
        }
    },
    methods:{
        addTodo(){
            this.todoList.push({id:id++, text:this.text})
            this.text =''
        },
        removeTodo(todo){
            this.todoList = this.todoList.filter((item) => item !== todo)
        }
    }
}
</script>