<template>
  <HelloWorld @click="fetchData" :users="this.users" msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
