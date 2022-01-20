<template>
  <Button @click="fetchUsers" :users="users" buttonText="Load all users" />
  <Button @click="reset" backgroundColor="red" buttonText="Delete all data" />
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "NavigationBar",
  components: {
    Button,
  },
  props: {
    fetchUsers: {
      type: Function,
    },
    reset: {
      type: Function,
    },
    users: {
      type: Array,
    },
  },
};
</script>
