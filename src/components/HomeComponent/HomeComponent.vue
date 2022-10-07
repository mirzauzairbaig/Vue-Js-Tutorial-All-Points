<template>
  <div class="Home">
    {{ name }}
    <h1>{{ a + b }}</h1>
    <HeaderComponent />
    <button @click="hideHandeler">Hide Component</button>
    <FirstComponent />
    <SecondComponent v-if="hideComp" />
    <ThiredComponent />
  </div>
</template>

<script>
import HeaderComponent from "./HeaderComponent.vue";
import FirstComponent from "./UserF.vue";
import SecondComponent from "./UserS.vue";
import ThiredComponent from "./UserT.vue";
export default {
  name: "HomeComponent",
  data() {
    return {
      name: "ValueLab",
      a: 5,
      b: 4,
      hideComp: true,
    };
  },
  methods: {
    hideHandeler() {
      this.hideComp = !this.hideComp;
    },
  },
  components: {
    HeaderComponent,
    FirstComponent,
    SecondComponent,
    ThiredComponent,
  },
};
</script>

<style>
.Home {
  background-color: rgb(248, 248, 248);
  border: 1px solid black;
  height: 700px;
}
</style>
