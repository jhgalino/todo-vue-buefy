<template>
  <div class="columns">
    <div class="column"></div>
    <div class="column is-two-thirds">
      <h1 class="content is-size-1 has-text-centered">To-do</h1>
      <inputField @submitTodo="submitTodo"></inputField>
      <br />
      <activityList :content="todo"></activityList>
    </div>
    <div class="column"></div>
  </div>
</template>

<script>
import inputField from "./InputField";
import activityList from "./ActivityList";

export default {
  data() {
    return {
      todo: "",
    };
  },
  components: {
    inputField,
    activityList,
  },
  methods: {
    submitTodo(value) {
      this.todo = value;
    },
  },
};
</script>

<style scoped>
</style>
