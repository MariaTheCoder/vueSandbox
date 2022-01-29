<template>
  <div class="Display">
    <UserList @loadUserPosts="loadPosts" :users="users" />
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
    loadPosts(data) {
      this.$emit("loadUserPosts", data);
    },
  },
};
</script>

<style scoped>
.Display {
  margin-top: 25px;
}
</style>
