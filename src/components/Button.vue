<template>
  <div class="btns">
    <button>{{ buttonText }}</button>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    buttonText: String,
    users: {
      type: Array,
      required: false,
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
button {
  height: 30px;
  width: 150px;
  margin: 10px 5px 10px 5px;
  background-color: hsl(200, 50%, 70%);
  border: transparent;
  border-radius: 5px 5px 5px 5px;
}
</style>
