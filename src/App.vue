<template>
  <div id="app">
    <keep-alive>
      <component :is="component"></component>
    </keep-alive>

    <button @click="component = 'form-one'">显示formone</button>
    <button @click="component = 'form-two'">显示formtwo</button>
  </div>
</template>

<script>
import FormOne from "./components/FormOne.vue";
import FormTwo from "./components/FormTwo.vue";
export default {
  name: "App",
  data() {
    return {
      component: "form-two"
    };
  },
  components: {
    "form-one": FormOne,
    "form-two": FormTwo
  }
};
</script>

<style></style>
