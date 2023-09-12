<template>
  <form @submit.prevent>
    <h3>Add post</h3>
    <my-input v-model="post.title" type="text" placeholder="Название" />
    <my-input v-model="post.body" type="text" placeholder="Название" />
    <my-button @click="createPost" style="align-self: end; margin-top: 15px"
      >Добавить пост</my-button
    >
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      console.log(this.post);
      this.$emit("create", this.post);
      this.post = {
        title: "",
        body: "",
      };
    },
  },
};
</script>

<style scoped>
h3 {
  color: #1802a6;
  text-align: center;
}

form {
  /* margin: 20px 40px; */
  display: flex;
  flex-direction: column;
}
</style>