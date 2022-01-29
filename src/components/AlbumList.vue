<template>
  <fieldset>
    <legend>Albums:</legend>
    <div v-if="albums.length > 0">
      <Album v-for="album in albums" :key="album.id" :album="album" />
    </div>
    <div v-else>No loaded Albums</div>
  </fieldset>
</template>

<script>
import Album from "./Album.vue";

export default {
  name: "AlbumList",
  props: {
    albums: Array,
  },
  components: {
    Album,
  },
};
</script>

<style scoped></style>
