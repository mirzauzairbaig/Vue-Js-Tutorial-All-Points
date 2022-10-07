<template>
  <h1>----Style Type----</h1>
  <h1 class="head">Style using Class selectore</h1>
  <h1 v-bind:style="{ color: 'red' }">Style in-line</h1>
  <h3>----Object----</h3>
  <button v-on:click="ColorHandeler()">Change Color</button>
  <h1 v-if="show">Object Style</h1>
  <h1 :class="{ display: show }">Object Style</h1>
  <h3>----Array----</h3>
  <h1 v-bind:class="ashow">Array Style</h1>
  <h1 v-bind:class="show ? Yshow : Nshow">Arrays Style Toggle</h1>
</template>
<script>
export default {
  name: "styleType",
  data() {
    return {
      show: true,
      ashow: "arrayDisplay",
      Yshow: "aYshow ",
      Nshow: "aNshow",
    };
  },
  methods: {
    ColorHandeler() {
      this.show = !this.show;
    },
  },
};
</script>
<style>
.head {
  background-color: aquamarine;
}
.display {
  background-color: blue;
}
.arrayDisplay {
  background-color: blueviolet;
}
.aYshow {
  background-color: aqua;
}
.aNshow {
  background-color: chartreuse;
}
</style>
