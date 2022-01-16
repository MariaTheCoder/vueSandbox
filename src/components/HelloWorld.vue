<template>
  <div class="hello" >
    <h1>{{ msg }}</h1>
    <User :users="users"/>
  </div>
</template>

<script>
import User from './User.vue';

export default {
  name: 'HelloWorld',
  props: {
    msg: String,
    users: Array,
  }, 
  components: {
    User,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
