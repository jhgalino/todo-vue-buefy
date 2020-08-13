<template>
  <div class="columns">
    <div class="column"></div>
    <div class="column is-two-thirds">
      <inputField @submitTodo="passToList"></inputField>
      <activityList :submittedTodo="todo"></activityList>
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
    passToList(value) {
      this.todo = value;
    },
  },
};
</script>

<style scoped></style>
