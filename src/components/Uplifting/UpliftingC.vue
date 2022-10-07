<template>
  <h1>Uplifting Child</h1>
  <button @click="funcChild">Update Ppparrent</button>
</template>
<script>
export default {
  name: "UpliftingC",
  methods: {
    funcChild() {
      console.log("Child");
      this.$emit("UpliftingProps", "Update Done...!");
    },
  },
};
</script>
