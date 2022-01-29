<template>
  <fieldset>
    <legend>Users:</legend>
    <div v-if="users.length > 0">
      <User
        @loadUserPosts="refireUserPosts"
        @passUserIdUp="refireUserId"
        v-for="user in users"
        :key="user.id"
        :user="user"
      />
    </div>
    <div v-else>No loaded Users</div>
  </fieldset>
</template>

<script>
import User from "./User.vue";

export default {
  name: "Users",
  components: {
    User,
  },
  props: {
    users: Array,
  },
  methods: {
    refireUserPosts(data) {
      this.$emit("loadUserPosts", data);
    },
    refireUserId(data) {
      this.$emit("passUserIdUp", data);
    },
  },
};
</script>

<style scoped>
fieldset {
  margin-top: 10px;
}
</style>
