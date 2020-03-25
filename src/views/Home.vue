<template>
  <div class="home">
    <TodoList :todos="todos" />
  </div>
</template>

<script>
import TodoList from "../components/TodoList";

export default {
  name: "home",
  components: {
    TodoList
  },
  created() {
    this.todos = this.$todos.getItems();
  },
  data() {
    return {
      todos: []
    };
  }
};
</script>
