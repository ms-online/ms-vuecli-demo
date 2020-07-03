<template>
  <div id="app">
    <FormHelper>
      <div slot="title">
        <h2>{{ title }}</h2>
        <p>Lorem ipsum dolor sit amet.</p>
      </div>

      <p slot="content">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat,
        blanditiis.
      </p>
    </FormHelper>
  </div>
</template>

<script>
import FormHelper from './components/FormHelper.vue';
export default {
  name: 'App',
  data() {
    return {
      title: '这是标题',
    };
  },
  components: {
    FormHelper,
  },
};
</script>

<style>
h2 {
  color: aqua;
}
</style>
