<template>
  <div>
    <p>{{ msg }}</p>
    <p class="primary">{{ primaryMsg }}</p>
  </div>
</template>

<script>
export default {
  name: "Greeting",
  data() {
    return {
      msg: "Hello World",
      primaryMsg: "Class color",
    };
  },
};
</script>

<style scoped>
p {
  color: red;
}

.primary {
  color: blue;
}
</style>
