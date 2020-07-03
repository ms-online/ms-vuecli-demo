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
    <button @click="deleteUsers()">删除</button>
  </div>
</template>

<script>
export default {
  //   props: ['users'],
  props: {
    users: {
      type: Array,
      required: true,
    },
    //   data() {
    //     return {
    //       users: 'users',
    //     };
  },

  methods: {
    deleteUsers() {
      this.users.pop();
    },
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
