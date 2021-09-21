<template>
  <div>
    <h1>
      <center>{{ like }}</center>
    </h1>

    <button @click="like += 1" class="btn btn-danger">layk+1</button>
    <button @click="like -= 1" class="btn btn-dark">layk-1</button>

    <input type="number" v-model="input1" />
    <input type="number" v-model="input2" />

    <button class="btn btn-info" @click="(input1 += input2), (input2 = '')">
      +
    </button>
  </div>
</template>

<script>
export default {
  data: () => ({
    like: 0,
    input1: 0,
    input2: 0,
  }),
};
</script>

<style>
</style>
