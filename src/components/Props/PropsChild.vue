<template>
  <div>
    <h1>{{ Name }}</h1>
    <h1>{{ object }}</h1>
    <table border="1px">
      <tr>
        <th>Name</th>
        <th>Email</th>
      </tr>
      <tr v-for="user in users" :key="user.name">
        <td>{{ user.name }}</td>
        <td>{{ user.Email }}</td>
      </tr>
    </table>
  </div>
</template>
<script>
export default {
  name: "PropsChild",
  props: ["Name", "object", "users"],
};
</script>
