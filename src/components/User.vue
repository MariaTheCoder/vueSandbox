<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"
  />
  <div @click="passUserId(user.id)">
    <div class="user-container">
      <img class="user-image item1" :src="picture" alt="profile-picture" />
      <p class="item2 user-name">{{ user.name }}</p>
      <i class="fa fa-close item3"></i>
      <p class="item4 user-username">@{{ user.username }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "User",
  props: {
    user: Object,
    picture: String,
  },
  emits: ["passUserIdUp"],
  methods: {
    passUserId(userId) {
      this.$emit("passUserIdUp", userId);
    },
  },
};
</script>

<style scoped>
.user-container {
  display: grid;
  grid-template-columns: 30% 60% 10%;
  grid-template-rows: repeat(2, auto);
  margin-bottom: 1em;
}

.user-name {
  margin: 0;
  font-weight: bold;
  margin: auto 0;
}

.user-username {
  margin: 0;
  font-size: 0.8em;
  color: #282828;
}

.item1 {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 3;
}

i {
  color: red;
  text-align: center;
}
.user-image {
  margin: auto 1em auto 0;
  max-width: 80px;
  height: auto;
  border-radius: 50%;
}
</style>
