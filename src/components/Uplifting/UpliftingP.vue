<template>
  <h1>Uplifting Parrent</h1>
  <h4>{{ title }}</h4>
  <UpliftingC v-on:UpliftingProps="funcParrent($event)" />
</template>
<script>
import UpliftingC from "./UpliftingC.vue";
export default {
  name: "UpliftingP",
  data() {
    return {
      title: "Mirza",
    };
  },
  methods: {
    funcParrent(title) {
      this.title = title;
    },
  },
  components: {
    UpliftingC,
  },
};
</script>
