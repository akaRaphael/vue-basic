<template>
  <button @click="handlerA(), handlerB()">
    Click me!!!
  </button>
</template>

<script>
export default {
  methods: {
    handlerA() {
      console.log('handler A!')
    },
    handlerB() {
      console.log('handler B!')
    },
  }
}
</script>