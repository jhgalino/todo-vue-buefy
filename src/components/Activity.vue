<template>
  <div class="columns">
    <div class="column">
      <p class="is-size-2">{{ text }}</p>
    </div>
    <div class="column">
      <button class="button is-size-4 is-pulled-right" @click="deleteThis">Delete</button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    text: String,
  },
  methods: {
    deleteThis() {
      this.$emit("delete", this.text);
    },
  },
};
</script>

<style scoped>
</style>
