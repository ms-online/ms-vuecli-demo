<template>
  <div id="app">
    <!-- 3.使用组件 -->
    <Header />
    <users v-bind:users="users" />
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
