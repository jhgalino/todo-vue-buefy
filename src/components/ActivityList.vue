<template>
  <div>
    <ul>
      <li v-for="(todo, index) in todos" :key="index">
        <todos :text="todo" @delete="deleteItem($event)"></todos>
      </li>
    </ul>
  </div>
</template>

<script>
import todos from "./Activity";

export default {
  data() {
    return {
      todos: [],
    };
  },
  props: {
    content: String,
  },
  components: {
    todos,
  },
  watch: {
    content: function (newval) {
      if (this.content != "") {
        this.todos.push(newval);
      }
    },
  },
  methods: {
    deleteItem(value) {
      this.todos = this.todos.filter((x) => x != value);
    },
  },
};
</script>

<style scoped>
</style>