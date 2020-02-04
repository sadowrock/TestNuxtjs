<template>
  <form @submit.prevent="onSubmit">
    <input type="text" id="text" v-model="text" placeholder="Search Jokes..." />
    <input type="submit" id="submit" value="Search Jokes" />
  </form>
</template>

<script>
export default {
  name: "SreachJokes",
  data() {
    return {
      text: ""
    };
  },
  methods: {
    onSubmit() {
      this.$emit("search-text", this.text);
      this.text = "";
    }
  }
};
</script>

<style>
#submit {
  border: 1px solid;
}
#text {
  border: 1px solid #222;
}
</style>
