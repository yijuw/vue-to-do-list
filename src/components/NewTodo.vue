<template>
    <div class="row">
        <div class="col-12">
            <form>
                <div class="form-group">
                    <label for="textarea" class="mt-3">Add a Todo</label>
                    <textarea class="form-control" id="textarea" rows="3" v-model="todo"></textarea>
                </div>
                <div class="form-group text-center">
                    <button class="btn btn-success" @click.prevent="addNew">Add Todo</button>
                </div>
            </form>
        </div>
        
    </div>
</template>
<script>
    export default {
       data: function() {
           return {
               todo: ''
           }
       },
       methods: {
           addNew() {
               this.$emit('todoAdded', this.todo);
               this.todo=""
           }
       }
    }
</script>
<style>
</style>