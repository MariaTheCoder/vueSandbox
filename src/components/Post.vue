<template>
  <div>
    <div v-if="post.id < 10">
      <p>Post 0{{ post.id }} - {{ post.title }}</p>
    </div>
    <div v-else>
      <p>Post {{ post.id }} - {{ post.title }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Post",
  data() {
    return {
      allPosts: [],
    };
  },
  props: {
    post: Object,
  },
};
</script>

<style scoped></style>
