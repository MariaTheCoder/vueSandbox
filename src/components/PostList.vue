<template>
  <fieldset>
    <legend>Posts:</legend>
    <div v-if="posts.length > 0">
      <Post v-for="post in posts" :key="post.id" :post="post" />
    </div>
    <div v-else>No loaded Posts</div>
  </fieldset>
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

<style scoped>
fieldset {
  margin-top: 10px;
}
</style>
