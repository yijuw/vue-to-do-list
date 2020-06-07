<template>
    <div class="row">
        <div class="col-md-8 offset-md-2 col-sm-12 my-4">
        <app-todo-list v-for="(todo, index) in todos" :key="todoList">
              <li class="list-group-item">{{ todo}} 
                  <button type="button" class="btn btn-outline-dark float-right" @click="deleteTodo(index)"><i class="fas fa-trash"></i></button>
              </li>
        </app-todo-list>
        </div>

    </div>
</template>
<script>
import TodoList from './Todos.vue'
export default {
    props: ['todos'],
    methods: {
        deleteTodo(index) {
            this.$emit('todoDeleted', index)
        }
    },
    components:{
             'app-todo-list': TodoList,
        }
}
</script>
<style scoped>
button {border-radius: 50%;}

</style>