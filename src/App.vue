<template>
  <h1>{{ computedMessage }}</h1>
  <h1>{{ computedMessage }}</h1>
  <h1>{{ computedMessage }}</h1>
  <h1>{{ computedMessage }}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello Computed!"
    }
  },
  computed: { 
    // computed는 연산된 data를 관리하는 공간이다. 
    // 아래의 computedMessage()는 메소드처럼 선언되었지만
    // data처럼 명시 및 사용됨 기억하자. 
    computedMessage() {
      return this.msg.split('').reverse().join('')
    }
  },
  methods: {
    reverseMessage() {
      return this.msg.split('').reverse().join('')
    }
  }
}
</script>

<style>
 h1{
   font-size: 50px;
 }
</style>