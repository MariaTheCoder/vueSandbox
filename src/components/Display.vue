<template>
  <div class="Display">
    <UserList :users="users" />
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
};
</script>

<style scoped></style>
