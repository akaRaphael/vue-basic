<template>
  <li>{{ name }}!!!</li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: '' //props의 name 속성은 반드시 default값을 설정해야한다.
    }
  }
}
</script>

<style scoped lang="scss">
  h1 {
    color: darkgreen;
  }
</style>