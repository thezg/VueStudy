<template>
  <input :value="modelValue" @input="updateInput" type="text" class="input" />
</template>

<script>
export default {
  name: "my-input",
  props: {
    modelValue: [String, Number],
  },
  methods: {
    updateInput(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style scoped>
.input {
  width: 100%;
  color: #984cfc;
  border: 1px solid #984cfc;
  margin-top: 20px;
  padding: 10px 15px;
}
.input::placeholder {
  color: #984cfc;
}
</style>