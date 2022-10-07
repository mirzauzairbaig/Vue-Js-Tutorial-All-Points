<template>
  <h1>If Else Component</h1>
  <button v-on:click="display()">{{ buttonName }}</button>
  <h4 v-if="show">Show ToGGle If Text</h4>
  <!-- <h4 v-else>Show ToGGle else Text</h4> -->
  <!-- <button @click="display()">toggle text</button> -->
</template>
<script>
export default {
  name: "IfElse",
  data() {
    return {
      show: true,
      buttonName: "Show",
    };
  },
  methods: {
    display() {
      this.show = !this.show;
      if (!this.show) {
        this.buttonName = "Hide";
      } else {
        this.buttonName = "Show";
      }
    },
  },
};
</script>
