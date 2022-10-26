<template>
  <section class="info">
    <form @submit.prevent="submitData">
      <label>Name: </label>
      <input type="text" v-model="name" />
      <br />
      <br />
      <label>Age: </label>
      <input type="text" v-model="age" />
      <br />
      <br />
      <button>Set User Data</button>
    </form>
  </section>
</template>

<script>
export default {
  emits: ["set-data"],
  data() {
    return {
      name: "",
      age: "",
    };
  },
  methods: {
    submitData() {
      this.$emit("set-data", this.name, this.age);
    },
  },
};
</script>