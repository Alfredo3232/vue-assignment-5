<template>
  <user-data @set-data="setUserData"></user-data>
  <active-user :username="user.name" :userage="user.age"></active-user>
</template>

<script>
export default {
  data() {
    return {
      user: {
        name: "",
        age: 0,
      },
    };
  },
  methods: {
    setUserData(name, age) {
      this.user = {
        name: name,
        age: +age,
      };
    },
  },
};
</script>

<style>
html {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
}
.info {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid whitesmoke;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
  padding: 15px;
  text-align: center;
}
</style>