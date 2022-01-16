<template>
    <div class="User">
        <div v-for="user in users" :key="user.id">
            User {{ user.id }} - {{ user.name }}
        </div>
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

<style>
</style>
