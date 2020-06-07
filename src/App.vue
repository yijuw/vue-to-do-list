<template>
    <div class="container">
        <app-header :todoCount="todos.length" :maxTodos="maxTodos"></app-header>
        <app-new-todo @todoAdded="newTodo"></app-new-todo>
        <app-todo-grid :todos="todos" @todoAdded="name=$event" @todoDeleted="deleteTodo"></app-todo-grid>
    </div>
</template>

<script>
import TodoGrid from './components/TodoGrid.vue';
import NewTodo from './components/NewTodo.vue';
import Header from './components/Header.vue'
    export default {
        data: function() {
            return {
                todos:['Coding:)', 'cooking'],
                maxTodos :20
            }
        },
        methods: {
            newTodo(todo) {
                if(this.todos.length >= this.maxTodos) {
                    return alert('Please delete one of your todos first!')
                }
                this.todos.push(todo)
            },
            deleteTodo(index){ 
                this.todos.splice(index, 1)
            }
        },
        components: {
            'app-todo-grid': TodoGrid,
            'app-new-todo': NewTodo,
            'app-header': Header
        }
    }
</script>

<style>
</style>
