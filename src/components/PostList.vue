<template>
  <div v-for="post in posts" :key="post.id">
    <p v-if="posts.length > 0">Post {{ post.id }} - {{ post.title }}</p>
  </div>
</template>

<script>
export default {
  name: "Posts",
  props: {
    posts: Array,
  },
};
</script>

<style scoped></style>
