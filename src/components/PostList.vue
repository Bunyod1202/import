<template>
  <div class="post" v-for="post in posts" v-bind:key="post">
    <div><strong>Name:</strong>{{ post.title }}</div>
    <div><strong>Text:</strong>{{ post.body }}</div>
  </div>
</template>

<script>
export default {
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style>
.post {
  padding: 15px;
  border: 2px solid teal;
  margin-top: 15px;
}
</style>
