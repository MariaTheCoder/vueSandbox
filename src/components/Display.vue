<template>
  <div class="Display">
    <User :users="users" />
    <Post :posts="posts" />
    <Album :albums="albums" />
  </div>
</template>

<script>
import User from "./User.vue";
import Post from "./Post.vue";
import Album from "./Album.vue";

export default {
  name: "Display",
  components: {
    User,
    Post,
    Album,
  },
  props: {
    posts: {
      type: Array,
    },
    users: {
      type: Array,
    },
    albums: {
      type: Array,
    },
  },
};
</script>

<style scoped></style>
