<template>
  <div class="hello" >
    <button>{{ msg }}</button>
    <User :users="users"/>
  </div>
</template>

<script>
import User from './User.vue';

export default {
  name: 'Button',
  props: {
    msg: String,
    users: { 
      type: Array, 
      required: true
    },
  }, 
  components: {
    User,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
