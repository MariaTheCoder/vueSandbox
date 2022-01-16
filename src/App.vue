<template>
  <Button @click="fetchData" :users="this.users" buttonText="Load all users"/>
  <Button @click="reset" buttonText="Delete all users"/>
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
    }, 
    reset() {
      this.users = [];
    }
  }
}
</script>

<style>
</style>
