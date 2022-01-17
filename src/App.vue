<template>
  <Button @click="fetchUsers" :users="this.users" buttonText="Load all users" />
  <Button @click="reset" :style="{ color: red }" buttonText="Delete all data" />
  <button :style="deleteButtonStyle">Am I red?</button>
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
      deleteButtonStyle: {
        color: "red",
      },
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
