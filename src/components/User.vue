<template>
    <div class="User">
        <p v-for="user in users" :key="user.id">
            User {{ user.id }} - {{ user.name }}
        </p>
    </div>
</template>

<script>
export default {
  name: 'User',
  props: {
    users: Array,
  }
}
</script>

<style scoped>
</style>
