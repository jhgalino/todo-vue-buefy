<template>
  <div><b-table :data="data" :columns="columns"></b-table></div
></template>

<script>
export default {
  props: {
    submittedTodo: String,
  },
  data() {
    return {
      data: [],
      columns: [
        {
          field: "todo",
          numeric: false,
        },
      ],
    };
  },
  watch: {
    submittedTodo: function(newval) {
      this.data.push({ todo: newval });
    },
  },
};
</script>

<style scoped></style>
