<template>
  <div v-for="album in albums" :key="album.id">
    <p v-if="albums.length > 0">Album {{ album.id }} - {{ album.title }}</p>
  </div>
</template>

<script>
export default {
  name: "Albums",
  props: {
    albums: Array,
  },
};
</script>

<style scoped></style>
