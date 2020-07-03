<template>
  <div class="users">
    <h1>Users.vue</h1>
    <h2>Users.vue</h2>
    <ul>
      <li v-for="(user, index) in users" :key="index">{{ user }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: ['Yellemy', 'Worley', 'Lucy', 'Tracy'],
    };
  },
};
</script>

<style scoped>
h1 {
  color: green;
}
</style>
