<template>
  <fieldset>
    <legend>Users:</legend>
    <div v-if="users.length > 0">
      <User
        @passUserIdUp="refireUserId"
        v-for="user in users"
        :key="user.id"
        :user="user"
        :picture="picture"
      />
    </div>
    <div v-else>No loaded Users</div>
  </fieldset>
</template>

<script>
import User from "./User.vue";

export default {
  name: "Users",
  data() {
    return {
      picture: "https://thispersondoesnotexist.com/image",
    };
  },
  components: {
    User,
  },
  props: {
    users: Array,
  },
  emits: ["passUserIdUp"],
  methods: {
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
