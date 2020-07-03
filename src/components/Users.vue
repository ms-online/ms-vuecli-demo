<template>
  <div class="users">
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

<style scoped></style>
