<template>
  <NavigationBar :fetchUsers="fetchUsers" :reset="reset" :users="this.users" />
  <Display :users="this.users" />
</template>

<script>
import Display from "./components/Display.vue";
import NavigationBar from "./components/NavigationBar.vue";

export default {
  name: "App",
  components: {
    Display,
    NavigationBar,
  },
  data() {
    return {
      users: {
        default: [],
      },
    };
  },
  emits: ["click"],
  methods: {
    fetchUsers() {
      this.$emit("click", () => {
        fetch("https://jsonplaceholder.typicode.com/users")
          .then((response) => response.json())
          .then((json) => (this.users = json));
      });
    },
    reset() {
      this.users = [];
    },
  },
};
</script>

<style></style>
