<template>
  <h1>For Loop</h1>
  <table border="1px">
    <tr>
      <td>Id</td>
      <td>Name</td>
      <td>Email</td>
    </tr>
    <tr v-for="user in users" :key="user.id">
      <td>{{ user.id }}</td>
      <td>{{ user.name }}</td>
      <td>{{ user.email }}</td>
    </tr>
  </table>
</template>
<script>
export default {
  name: "forLoop",
  data() {
    return {
      users: [
        { id: 1, name: "Malik", email: "malik@gmail.com" },
        { id: 2, name: "Rohit", email: "rohit@gmail.com" },
        { id: 3, name: "Abdul", email: "abduk@gmail.com" },
        { id: 4, name: "Rohan", email: "rohit@gmail.com" },
      ],
    };
  },
};
</script>
