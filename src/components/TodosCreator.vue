<script setup>
import { reactive, ref, defineEmits } from "vue";
const emit = defineEmits(["create-todo"]);

const todo = ref("");

const createTodo = () => {
  emit("create-todo", todo.value);
  todo.value = "";
};
// const todoState = reactive ({
//     todo: "testing",
// });
// export default {
//     data: function () {
//         return {
//             todo: "test"
//         };
//     }
// }
</script>

<template>
    <div class="input-wrap">
      <input type="text" v-model="todo" />
      <button @click="createTodo()">Create</button>
    </div>
</template>

<style lang="scss" scoped>
.input-wrap {
  display: flex;
  transition: 250ms ease;
  border: 2px solid #41b080;
  margin-top: 15px;

  &:focus-within {
    box-shadow: 0 -4px 6px -1px rgb(0 0 0 / 0.1),
      0 -2px 4px -2px rgba(110, 110, 110, 0.1);
  }

  input {
    width: 100%;
    padding: 8px 6px;
    border: none;

    &:focus {
      outline: none;
    }
  }

  button {
    padding: 8px 16px;
    border: none;
  }
}
</style>