<template>
  <div>
    <p>{{ msg }}</p>
    <p class="primary">{{ primaryMsg }}</p>
    <p v-if="age > 25">{{ msg }}</p>
    <p v-else>Must be max 25 years old to see this message</p>
  </div>
</template>

<script>
export default {
  name: "Greeting",
  props: ["age"],
  data() {
    return {
      msg: "Hello World",
      primaryMsg: "Class color",
    };
  },
};
</script>

<style lang="scss" scoped>
p:hover {
  color: darken(red, 15%);
}

.primary {
  color: blue;
}
</style>
