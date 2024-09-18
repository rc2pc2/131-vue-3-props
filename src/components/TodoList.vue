<script>
import TodoListItem from './TodoListItem.vue';

export default {
    data() {
        return {
            todoList : [
                {
                    text: "Fare la spesa",
                    done: false,
                },
                {
                    text: "Fare i compiti",
                    done: true,
                },
                {
                    text: "Stendere i panni",
                    done: true,
                },
                {
                    text: "Pagare l'assicurazione del lanciafiamme",
                    done: false,
                },
                {
                    text: "Andare in palestra in accappatoio",
                    done: false,
                },
                {
                    text: "Ballare in una fontana antica senza rovinarla",
                    done: false,
                },
            ],
        }
    },
    components:{
        TodoListItem
    }
}
</script>

<!-- {
    text: "Ballare in una fontana antica senza rovinarla",
    done: false,
}, -->
<template>
    <h1>
        Todolist
    </h1>
    
    <section class="todo-list">
        <ul>
            <TodoListItem v-for="(todoItem, index) in todoList" :key="index"
                :content="todoItem.text"
                :status="todoItem.done"
            /> 
        </ul>
    </section>
</template>

<style scoped>
</style>