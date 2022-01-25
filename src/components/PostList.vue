<template>
  <div v-if="posts.length > 0">
    <Post v-for="post in posts" :key="post.id" :post="post" />
  </div>
  <div v-else>No loaded Posts</div>
</template>

<script>
import Post from "./Post.vue";

export default {
  name: "PostList",
  props: {
    posts: Array,
  },
  components: {
    Post,
  },
};
</script>

<style scoped></style>
