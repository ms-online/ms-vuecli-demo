<template>
  <div class="users">
    <ul>
      <li
        @click="user.show = !user.show"
        v-for="(user, index) in users"
        :key="index"
      >
        <h3>{{ user.name }}</h3>
        <h4 v-show="user.show">{{ user.age }}</h4>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { name: 'Yellemy1', age: 25, show: false },
        { name: 'Yellemy2', age: 25, show: false },
        { name: 'Yellemy3', age: 25, show: false },
        { name: 'Yellemy4', age: 25, show: false },
        { name: 'Yellemy5', age: 25, show: false },
        { name: 'Yellemy6', age: 25, show: false },
        { name: 'Yellemy7', age: 25, show: false },
        { name: 'Yellemy8', age: 25, show: false },
      ],
    };
  },
};
</script>

<style scoped>
.users {
  width: 100%;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0 20px;
  box-sizing: border-box;
}

ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}

li {
  flex-grow: 1;
  flex-basis: 200px;
  text-align: center;
  padding: 30px;
  border: 1px solid #222;
  margin: 10px;
}
</style>
