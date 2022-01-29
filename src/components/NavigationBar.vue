<template>
  <div class="button-container">
    <Button @click="fetchUsers" :users="users" buttonText="Load all users" />
    <Button @click="fetchPosts" :posts="posts" buttonText="Load all posts" />
    <Button
      @click="fetchAlbums"
      :albums="albums"
      buttonText="Load all albums"
    />
    <Button
      class="delete"
      @click="reset"
      backgroundColor="red"
      textColor="white"
      buttonText="Delete all data"
    />
  </div>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "NavigationBar",
  components: {
    Button,
  },
  props: {
    fetchAlbums: {
      type: Function,
    },
    fetchPosts: {
      type: Function,
    },
    fetchUsers: {
      type: Function,
    },
    reset: {
      type: Function,
    },
    users: {
      type: Array,
    },
    posts: {
      type: Array,
    },
    albums: {
      type: Array,
    },
  },
};
</script>

<style scoped>
.button-container {
  display: grid;
  grid-template-columns: auto;
  /* repeat(3, auto); */
  grid-template-rows: repeat(2, 50px);
  grid-gap: 10px;
}

.delete {
  grid-column-start: 1;
  grid-column-end: 4;
}
</style>
