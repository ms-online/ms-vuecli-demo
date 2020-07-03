<template>
  <div id="app">
    <!-- 3.使用组件 -->
    <Header />
    <users />
    <Footer />
  </div>
</template>

<script>
// 1.局部引用组件
import Header from './components/Header.vue';
import Users from './components/Users.vue';
import Footer from './components/Footer.vue';
export default {
  name: 'App',
  components: {
    // 2.注册组件
    Header,
    // 'ms-users': Users,
    users: Users,
    Footer,
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
