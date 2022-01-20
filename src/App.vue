<template>
  <NavigationBar
    :fetchUsers="fetchUsers"
    :fetchPosts="fetchPosts"
    :fetchAlbums="fetchAlbums"
    :reset="reset"
    :users="this.users"
    :posts="this.posts"
    :albums="this.albums"
  />
  <Display :users="this.users" :posts="this.posts" :albums="this.albums" />
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
      albums: {
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
    fetchAlbums() {
      fetch("https://jsonplaceholder.typicode.com/albums")
        .then((response) => response.json())
        .then((json) => (this.albums = json));
    },
    reset() {
      this.users = [];
      this.posts = [];
      this.albums = [];
    },
  },
};
</script>

<style></style>
