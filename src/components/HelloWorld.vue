<template>
  <!-- HTML结构：只能有一个根标签 -->
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>{{ wechat }}</p>
    <p>{{ greeting() }}</p>
  </div>
</template>

<script>
// js部分 逻辑部分
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: '米修在线',
      wechat: '12345',
    };
  },
  methods: {
    greeting() {
      return `大家好，我叫${this.msg}, 我的微信号是${this.wechat}`;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/*css样式  */
</style>
