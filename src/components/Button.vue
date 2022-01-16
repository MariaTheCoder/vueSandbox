<template>
  <div class="hello" >
    <button>{{ buttonText }}</button>
    <User :users="users"/>
  </div>
</template>

<script>
import User from './User.vue';

export default {
  name: 'Button',
  props: {
    buttonText: String,
    users: { 
      type: Array, 
      required: false
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
