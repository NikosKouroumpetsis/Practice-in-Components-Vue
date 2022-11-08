<template>
  <button type="button" @click="onClickAge">Update Age Event</button>
  <button type="button" @click="ageChangeFn(10)">Update Age CB</button>
  <p>The user is {{ age }} year's old</p>
  <p>Doubled age: {{ ageDoubled }}</p>
</template>

<script>
export default {
  name: "User",
  props: {
    age: {
      type: Number,
      //   required: true,
      //   default: 40,
      validator(value) {
        // this.onClickAge();
        return value < 130;
      },
    },
    ageChangeFn: Function,
  },
  emits: ["age-change"],
  computed: {
    ageDoubled() {
      return this.age * 2;
    },
  },
  methods: {
    onClickAge() {
      this.$emit("age-change", 2);
    },
  },
};
</script>

<style scoped></style>
