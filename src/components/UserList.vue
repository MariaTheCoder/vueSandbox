<template>
  <div v-for="user in users" :key="user.id">
    <p v-if="users.length > 0">User {{ user.id }} - {{ user.name }}</p>
  </div>
</template>

<script>
export default {
  name: "Users",
  props: {
    users: Array,
  },
};
</script>

<style scoped></style>
