<template>
  <h1>Input Data Bind</h1>
  <input type="text" v-model="message" />
  <h1>{{ message }}</h1>
</template>
<script>
export default {
  name: "InputDataBind",
  data() {
    return {
      message: "Hi",
    };
  },
};
</script>
