<template>
  <form>
    <label>Name: </label>
    <input type="text" v-model="name" />
    <br />
    <br />
    <label>Age: </label>
    <input type="text" v-model="age" />
  </form>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      age: 0,
    };
  },
  methods: {
    setName(event) {
      this.name = event.target.value;
    },
  },
};
</script>