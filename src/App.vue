<template>
  <Button @click="fetchData" :users="this.users" buttonText="Load all users"/>
  <Button buttonText="Delete all users"/>
</template>

<script>
import Button from './components/Button.vue'

export default {
  name: 'App',
  components: {
    Button
  },
  data() {
    return {
      users: [],
    }
  },
  methods: {
    fetchData() {
      fetch('https://jsonplaceholder.typicode.com/users')
      .then(response => response.json())
      .then(json => this.users = json)
    }
  }
}
</script>

<style>
</style>
