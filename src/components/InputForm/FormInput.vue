<template>
  <div></div>
  <h1>Form With Checkbox and radio button in Vue js</h1>
  <input type="text" placeholder="name" v-model="signUp.userName" /><br /><br />
  <input
    type="password"
    placeholder="Password"
    v-model="signUp.password"
  /><br /><br />
  <h4>Chose Hobbies</h4>
  <input
    type="checkbox"
    id="football"
    value="football"
    v-model="signUp.hobbies"
  />
  <lable for="football">FootBall</lable>
  <input
    type="checkbox"
    id="circket"
    value="circket"
    v-model="signUp.hobbies"
  />
  <lable for="circket">CirCket</lable><br /><br />
  <h4>Chose Jender</h4>
  <input type="radio" id="male" value="male" v-model="signUp.gender" />
  <lable for="male">Male</lable>
  <input type="radio" id="female" value="female" v-model="signUp.gender" />
  <lable for="female">Female</lable><br /><br />
  <button v-on:click="submituser">Submit</button>
</template>
<script>
export default {
  name: "InputForm",
  data() {
    return {
      signUp: {
        userName: "",
        password: "",
        hobbies: [],
        gender: [],
      },
    };
  },
  methods: {
    submituser() {
      console.log(this.signUp);
    },
  },
};
</script>
