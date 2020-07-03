<template>
  <div @click="changeTitle()" class="header">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
  },
  data() {
    return {
      //   title: 'Vue Components Demo',
    };
  },
  methods: {
    changeTitle() {
      // this.title = 'Yellemy'; 不能直接在子组件修改父组件的值
      // 通过注册事件  参数1:事件名称，参数2...:传递的值
      this.$emit('titleChanged', 'Yellemy');
    },
  },
};
</script>

<style scoped>
.header {
  background: grey;
  padding: 10px;
}

h1 {
  color: #fff;
  text-align: center;
}
</style>
