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
    textColor: {
      type: String,
      default: "black",
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
  height: 100%;
  width: 100%;
  background-color: v-bind(backgroundColor);
  font-size: 20px;
  font-weight: bold;
  color: v-bind(textColor);
  border: transparent;
  border-radius: 5px 5px 5px 5px;
}
</style>
