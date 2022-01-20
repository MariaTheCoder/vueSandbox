<template>
  <div class="button-container">
    <div class="navigational-buttons">
      <Button @click="fetchUsers" :users="users" buttonText="Load all users" />
      <Button @click="fetchPosts" :posts="posts" buttonText="Load all posts" />
      <Button
        @click="fetchAlbums"
        :albums="albums"
        buttonText="Load all albums"
      />
    </div>
    <Button @click="reset" backgroundColor="red" buttonText="Delete all data" />
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
  },
};
</script>

<style scoped>
.button-container {
  display: flex;
  flex-direction: column;
}
.navigational-buttons {
  display: flex;
  flex-direction: row;
}
</style>
