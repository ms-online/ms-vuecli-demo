<template>
  <div id="app">
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

<style></style>
