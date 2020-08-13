<template>
  <div>
    <b-field>
      <b-input
        v-model.lazy="input"
        placeholder="What do you want to do?"
        type="text"
        size="is-large"
        expanded
        @keyup.native.enter="submit"
      ></b-input>
      <p class="control">
        <b-button type="submit" class="button is-large" @click="submit">Add</b-button>
      </p>
    </b-field>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      input: "",
    };
  },
  methods: {
    submit() {
      if (this.input != "") {
        this.$emit("submitTodo", this.input);
      }
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
