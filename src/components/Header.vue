<template>
<div class="row">
    <div class="col-12">
        <h3 class="text-center my-4">To-Do List</h3>
        <div class="progress">
            <div class="progress-bar bg-info" role="progressbar" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100" 
            :style="{width: (todoCount / maxTodos) * 100 + '%'}">
             {{todoCount}} / {{maxTodos}}
            </div>
        </div>
    </div>
</div>

</template>
<script>
export default {
    props: ['todoCount', 'maxTodos']
}
</script>