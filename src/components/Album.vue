<template>
  <div class="Album">
    <p v-for="album in albums" :key="album.id">
      Album {{ album.id }} - {{ album.title }}
    </p>
  </div>
</template>

<script>
export default {
  name: "Album",
  props: {
    albums: Array,
  },
};
</script>

<style scoped></style>
