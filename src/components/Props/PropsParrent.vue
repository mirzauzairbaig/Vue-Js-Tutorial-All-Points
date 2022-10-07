<template>
  <h1>PropsParrent</h1>
  <h6>1-String</h6>
  <PropsChiled Name="Mirza" />
  <h6>2-Object</h6>
  <PropsChiled v-bind:object="Usernaem" />
  <h6>3-Array</h6>
  <PropsChiled v-bind:users="users" />
</template>
<script>
import PropsChiled from "./PropsChild.vue";
export default {
  name: "PropsParrent",
  components: {
    PropsChiled,
  },
  data() {
    return {
      Usernaem: "Vue Js",
      users: [
        { name: "Khan", Email: "khan@gmail.com" },
        { name: "Pathan", Email: "pathan@gmail.com" },
        { name: "Rahul", Email: "rahul@gmail.com" },
        { name: "Rohit", Email: "rohit@gmail.com" },
      ],
    };
  },
};
</script>
