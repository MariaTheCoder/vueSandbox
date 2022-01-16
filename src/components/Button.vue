<template>
  <div class="hello" >
    <button>{{ buttonText }}</button>
  </div>
</template>

<script>
export default {
  name: 'Button',
  props: {
    buttonText: String,
    users: { 
      type: Array, 
      required: false
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
