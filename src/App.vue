<script setup>
import { RouterView } from "vue-router";
import TodoHeader from "./components/TodoHeader.vue";
</script>

<template>
  <TodoHeader />
  <RouterView />
</template>

<style lang="scss">
* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  font-family: system-ui;
  list-style: none;
}
a{
  text-decoration: none;
}
.container {
  max-width: 1100px;
  margin: 0 auto;
}
</style>
