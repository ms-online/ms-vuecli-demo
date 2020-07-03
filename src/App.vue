<template>
  <div id="app">
    <h1>App.vue</h1>
    <h2>App.vue</h2>
    <!-- 3.使用组件 -->
    <users />
  </div>
</template>

<script>
// 1.局部调用组件
import Users from './components/Users.vue';
export default {
  name: 'App',
  components: {
    // 2.注册组件
    // 'ms-users': Users,
    users: Users,
  },
};
</script>

<style>
h1 {
  color: red;
}

h2 {
  color: aqua;
}
</style>
