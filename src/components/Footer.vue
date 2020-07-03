<template>
  <footer>
    <p>{{ Copyright }}</p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      Copyright: 'Copyright 2020',
    };
  },
};
</script>

<style scoped>
footer {
  background: grey;
  padding: 10px;
}

p {
  color: #fff;
  text-align: center;
}
</style>
