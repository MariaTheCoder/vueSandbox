<template>
  <NavigationBar
    :fetchUsers="fetchUsers"
    :fetchPosts="fetchPosts"
    :reset="reset"
    :users="this.users"
    :posts="this.posts"
  />
  <Display :users="this.users" :posts="this.posts" />
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
      posts: {
        default: [],
      },
    };
  },
  methods: {
    fetchUsers() {
      fetch("https://jsonplaceholder.typicode.com/users")
        .then((response) => response.json())
        .then((json) => (this.users = json));
    },
    fetchPosts() {
      fetch("https://jsonplaceholder.typicode.com/posts")
        .then((response) => response.json())
        .then((json) => (this.posts = json));
    },
    reset() {
      this.users = [];
      this.posts = [];
    },
  },
};
</script>

<style></style>
