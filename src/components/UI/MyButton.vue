<template>
  <button class="addBtn">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "my-button",
};
</script>

<style scoped>
.addBtn {
  padding: 10px 15px;
  color: #984cfc;
  border: 1px solid #984cfc;
  background: none;
}
</style>