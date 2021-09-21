<template>
  <form @submit.prevent>
    <h4>sazdat post</h4>
    <input v-model="post.title" class="input" type="text" placeholder="Name" />
    <input v-model="post.body" class="input" type="text" placeholder="Text" />
    <button id="btn" class="btn" @click="createPost">sazdat</button>
  </form>
</template>

<script>
export default {
  data: () => ({
    post: {
      title: "",
      body: "",
    },
  }),
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("cteate", this.post);
      this.post = {
        title: "",
        body: "",
      };
    },
  },
};
</script>

<style>
.form {
  display: flex;
  flex-direction: column;
}
.input {
  width: 100%;
  border: 1px solid teal;
  padding: 10px 15px;
}
#btn {
  margin-top: 15px;
  align-self: flex-end;
  padding: 10px 15px;
  background: none;
  color: teal;
  border: 1px solid teal;
}
</style>
