<template>
  <div class="Display">
    <UserList @passUserIdUp="passUserId" :users="users" />
    <PostList :posts="posts" />
    <AlbumList :albums="albums" />
  </div>
</template>

<script>
import UserList from "./UserList.vue";
import PostList from "./PostList.vue";
import AlbumList from "./AlbumList.vue";

export default {
  name: "Display",
  components: {
    UserList,
    PostList,
    AlbumList,
  },
  data() {
    return {
      postsByUser: [],
    };
  },
  props: {
    posts: {
      type: Array,
    },
    users: {
      type: Array,
    },
    albums: {
      type: Array,
    },
  },
  methods: {
    passUserId(userId) {
      this.$emit("passUserIdUp", userId);
    },
  },
};
</script>

<style scoped>
.Display {
  margin-top: 25px;
}
</style>
