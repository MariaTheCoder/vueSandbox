<template>
  <Button @click="fetchUsers" :users="this.users" buttonText="Load all users" />
  <Button @click="reset" backgroundColor="red" buttonText="Delete all data" />
  <Display :users="this.users" />
</template>

<script>
import Button from "./components/Button.vue";
import Display from "./components/Display.vue";

export default {
  name: "App",
  components: {
    Button,
    Display,
  },
  data() {
    return {
      users: [],
    };
  },
  methods: {
    fetchUsers() {
      fetch("https://jsonplaceholder.typicode.com/users")
        .then((response) => response.json())
        .then((json) => (this.users = json));
    },
    reset() {
      this.users = [];
    },
  },
};
</script>

<style></style>
