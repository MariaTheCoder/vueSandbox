<template>
  <div class="btns">
    <button>
      {{ buttonText }}
    </button>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: {
    backgroundColor: {
      type: String,
      default: "#0099CC70",
    },
    buttonText: {
      type: String,
    },
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
  min-width: 200px;
  margin: 10px 5px 10px 5px;
  background-color: v-bind(backgroundColor);
  border: transparent;
  border-radius: 5px 5px 5px 5px;
}
</style>
