<template>
  <div>
    <slot name="title"></slot>
    <h1>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nihil,
      laboriosam?
    </h1>
    <slot name="content"></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      //   title: '这是标题', //不能在引用的地方设置属性值
    };
  },
};
</script>

<style scoped>
/* h2 {
  color: aqua;
} */
</style>
