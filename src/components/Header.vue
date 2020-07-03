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
      this.title = 'Yellemy';
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
