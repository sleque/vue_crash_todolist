<template>
    <div>
        <div v-bind:key="todosObjects.id" v-for="todosObjects in todosObjects">
           <TodoItem v-bind:todosObjects="todosObjects" v-on:del-todo="$emit('del-todo', todosObjects.id)"/>
        </div>
    </div>
</template>

<script>
import TodoItem from './TodoItem.vue';

export default {
    name: "Todos",
    components: {
        TodoItem
    },
    props: ["todosObjects"]
}
</script>

<style scoped>

</style>
