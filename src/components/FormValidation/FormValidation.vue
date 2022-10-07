<template>
  <h1>Form Validation</h1>
  <p v-if="error.length">
    <b>Plese Correct The Folling error</b>
    <ul>
      <li v-for="e in error" v-bind:key="e.id">{{ e }}</li>
    </ul>
  </p>
  <form @submit="login">
    <input type="text" placeholder="User Nnme" v-model="userName" /><br /><br />
    <input type="password" placeholder="Password" v-model="Password" /><br /><br />
    <button type="submit">Submit</button>
  </form>
</template>
<script>
export default {
  name: "FormValidation",
  data() {
    return {
      error: [],
      userName: null,
      Password: null,
    };
  },
  methods: {
    login(e) {
      if (this.userName && this.Password) {
        console.log("Submit...!");
      }
      if (!this.userName) {
        this.error.push("Please Enter Valid Name");
      }
      if (!this.Password) {
        this.error.push("Please Enter Valid Password");
      }
      console.log("Hello", e);
      e.preventDefault();
    },
  },
};
</script>
