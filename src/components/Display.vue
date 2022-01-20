<template>
  <div class="Display">
    <User :users="users" />
    <Post :posts="posts" />
  </div>
</template>

<script>
import User from "./User.vue";
import Post from "./Post.vue";

export default {
  name: "Display",
  components: {
    User,
    Post,
  },
  props: {
    posts: {
      type: Array,
    },
    users: {
      type: Array,
    },
  },
};
</script>

<style scoped></style>
