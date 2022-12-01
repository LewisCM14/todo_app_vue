<template>
    <h1>Todo List</h1>
    <todo-form @send-message="createTodo"></todo-form>
</template> 

<script lang="ts">
import { ElMessage } from 'element-plus';
import { Options, Vue } from 'vue-class-component';
import TodoForm from './TodoForm.vue';

@Options({
    components: {
        TodoForm,
    }
})
export default class TodoList extends Vue{
    async createTodo(todo: any){
        console.log("Todo", todo)
        ElMessage({
            message: "Todo Created",
            type: "success",
        })
    }
}
</script>