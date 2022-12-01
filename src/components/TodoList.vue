<template>
    <h1>Todo List</h1>
    <todo-form></todo-form>
</template> 

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import TodoForm from './TodoForm.vue';

@Options({
    components: {
        TodoForm,
    }
})
export default class TodoList extends Vue{
    
}
</script>