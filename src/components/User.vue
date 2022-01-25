<template>
  <div @click="postsByUser(user.id)">
    <div v-if="user.id < 10">
      <p>User 0{{ user.id }} - {{ user.name }}</p>
    </div>
    <div v-else>
      <p>User {{ user.id }} - {{ user.name }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "User",
  data() {
    return {
      userPosts: [],
    };
  },
  props: {
    user: Object,
  },
  methods: {
    postsByUser(userId) {
      fetch(`https://jsonplaceholder.typicode.com/posts?userId=${userId}`)
        .then((response) => response.json())
        .then((json) => {
          this.userPosts = json;
          this.passUserPosts();
          this.passUserId(userId);
        });
    },
    passUserPosts() {
      this.$emit("loadUserPosts", this.userPosts);
    },
    passUserId(userId) {
      this.$emit("passUserIdUp", userId);
    },
  },
};
</script>

<style scoped></style>
