<template>
  <div>
    <div v-if="album.id < 10">
      <p>Album 0{{ album.id }} - {{ album.title }}</p>
    </div>
    <div v-else>
      <p>Album {{ album.id }} - {{ album.title }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Album",
  data() {
    return {
      //
    };
  },
  props: {
    album: Object,
  },
};
</script>

<style scoped></style>
