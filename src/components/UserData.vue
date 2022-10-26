<template>
  <section class="info">
    <form>
      <label>Name: </label>
      <input type="text" v-model="name" />
      <br />
      <br />
      <label>Age: </label>
      <input type="number" v-model="age" />
    </form>
  </section>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      age: null,
    };
  },
  methods: {
    setName(event) {
      this.name = event.target.value;
    },
    setAge(event) {
      this.age = event.target.value;
    },
  },
};
</script>