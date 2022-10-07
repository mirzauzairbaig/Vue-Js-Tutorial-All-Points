<template>
  <h1>Hii</h1>
  <h3>Developer Name:{{ name }}</h3>
  <button @click="data">Call</button>
  <button @click="buttonHandelore">If Button</button>
  <h4 v-if="show">If Condition</h4>
  <h4 v-else>else Condition</h4>
  <button @click="funck('Hi mirze')">Call Function</button>
</template>
<script>
export default {
  name: "DayThree",
  props: {
    name: String,
  },
  data() {
    return {
      show: "true",
      buttoClick: "show",
    };
  },
  methods: {
    data() {
      console.log("Call Console");
    },
    funck(Call) {
      alert(Call);
    },
    buttonHandelore() {
      this.show = !this.show;
    },
  },
};
</script>
