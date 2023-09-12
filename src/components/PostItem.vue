<template>
  <div class="post">
    <div>
      <div class="postTitle">
        <strong>{{ post.title }}</strong>
      </div>
      <div class="postDescription">
        <strong>Description</strong> {{ post.body }}
      </div>
    </div>
    <div>
      <my-button @click="$emit('remove', post)">Delete</my-button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.post {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px;
  margin: 20px;
  border: 2px solid #984cfc;
}

strong {
  color: #1802a6;
  font-size: 16px;
}
</style>