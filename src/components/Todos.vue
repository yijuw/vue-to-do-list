<template>
    <div class="card">
        <div class="list-group todo">
            <slot></slot>
        </div>


    </div>
</template>
<script>
export default {
    
}
</script>
<style>
    .todo{
        cursor: pointer;
    }
    .todo:hover {
        background: #ffe2e2;
    }

</style>