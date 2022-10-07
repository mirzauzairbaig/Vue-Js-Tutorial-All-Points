<template>
  <h1>Hello This Is Home Component</h1>
  <h2>Props : {{ data }}</h2>
  <h2>Props : {{ msg }}</h2>
  <button v-on:click="hello">Call Function</button>
  <button v-on:click="nameHandler">Call Name</button>
</template>
<script>
export default {
  name: "HomeComp",
  props: {
    data: String,
    msg: String,
  },
  methods: {
    hello() {
      console.log("Call Function");
    },
    nameHandler() {
      console.log("My Name Is Mirza Uzair Ullah Baig");
    },
  },
};
</script>
