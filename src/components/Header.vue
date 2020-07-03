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

  // 生命周期函数（钩子函数）
  beforeCreate() {
    alert('这时实例还没有被创建，所以无法知道 data，也不能用 watch 监听；');
  },

  created() {
    alert('这时实例已经创建，可以得到 data，调用 watch，但是页面显示空白');
  },

  beforeMount() {
    alert('页面挂载前，此时页面显示空白，但是 render 函数被首次调用；');
  },

  mounted() {
    alert('页面挂载了，这时可以看到内容，也可以访问 dom；');
  },

  beforeUpdate() {
    alert('数据更新前，也就是虚拟 DOM 打补丁前；这时访问到的还是原有的 DOM；');
  },

  updated() {
    alert('数据已经更新完毕，重新渲染页面。');
  },

  beforeDestroy() {
    alert('离开页面之前被调用，清除定时器，或第三方的一些 DOM 结构；');
  },

  destroyed() {
    alert('实例已经完全被销毁。');
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
