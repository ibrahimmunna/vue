<template>
<h1>Computed Property</h1>
<form @submit.prevent="addTodo"> <!--To call the addTodo method while submitting-->
<input v-model='newTodo'/> <!-- Copy the new input text-->
<button>Add ToDo</button>
</form>    
<ul>
    
    <li v-for='todo in filterdTodos' :key='todo.id'> <!--running for loops for each task-->
        <input type="checkbox" v-model="todo.done"> <!--checking either the task is done or not-->
        <span :class="{done : todo.done}">{{todo.text}}</span> <!--using the css class and if it is done then apply it-->
        <button @click="removeTodo(todo)">Remove ToDo</button> <!--to call the removeTodo method with a parameter todo-->
    </li>
</ul> 
<button @click="hideCompleted = !hideCompleted">
{{hideCompleted ? 'Show all' : 'Hide Completed'}}
</button><!--Toggle between hideCompleted and show all & filter the completed task-->
</template>

<script>
let id = 0 //to give a uniqe id for the each task 
export default{
    name:'ComputedProperty',
    data(){
    return{
        newTodo:'',
        hideCompleted: false,
        todos:[
            {id: id++, text: 'Task 1', done: false} //task information
        ]

    }
},
computed:{
    filterdTodos(){
        return this.hideCompleted ? this.todos.filter((task) => !task.done) //to filte the tasks for hiding
        :this.todos
    }
},
methods:{
    addTodo(){
        this.todos.push({id:id++, text:this.newTodo, done: false}) //adding new task from the user input
    },
    removeTodo(todo){
        this.todos = this.todos.filter((task) => task !==todo) //remove a particular task
    }

}

}


</script>
<style scoped>
.done{
    text-decoration: line-through;
}
</style>