<template>
  <h1>Mirza</h1>
  <h3>Props:{{ flow }}</h3>
  <button v-on:click="callFunc('Parameter Pass!')">Call Function Pass parmetar</button>
</template>
<script>
export default {
  name: "DayTwo",
  props: {
    flow: String,
  },
  methods: {
    callFunc(data) {
      alert(data);
    },
  },
};
</script>
