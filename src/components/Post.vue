<template>
  <div class="Post">
    <p v-for="post in posts" :key="post.id">
      Post {{ post.id }} - {{ post.title }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Post",
  props: {
    posts: Array,
  },
};
</script>

<style scoped></style>
