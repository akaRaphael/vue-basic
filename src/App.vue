<template>
  <button @click="handler">
    Click me!!!
  </button>
  <h1 v-show="isShow">
    Hello?!
  </h1>
</template>

<script>
export default {
  data() {
    return {
      isShow: false,
      count: 0
    }
  },
  methods: {
    handler() {
      this.isShow = !this.isShow
      this.count += 1
    }
  }
}
</script>

<style>
  h1, button {
    font-size: 30px;
    margin-top: 5%;
    margin-left: 5%;
  }
</style>