<script setup>
import { reactive, ref } from "vue";
import { uid } from "uid";


import TodosCreator from "../components/TodosCreator.vue";
const todoList = ref([]);

const createTodo = (todo) => {
  todoList.value.push({
    id: uid(),
    todo,
    isCompleted: false,
    isEditing: null
  });
  console.log(todoList.value);
}
</script>

<template>
  <main>
    <h1>Create Todo</h1>
    <TodosCreator @create-todo="createTodo"></TodosCreator>
    <ul v-for="todoList in todoLists">
      <li>{{ todo }} + "hhhhhh"</li>
    </ul>
  </main>
</template>
<style scoped lang="scss">
main {
  display: flex;
  flex-direction: column;
  max-width: 500px;
  width: 100%;
  margin: 0 auto;
  padding: 40px 16px;

  h1 {
    margin-bottom: 16px;
    text-align: center;
    color: #333;
  }
}
</style>
