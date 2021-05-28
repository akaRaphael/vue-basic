<template>
  <MyBtn
    class="redBtn"
    style="color:red;"
    color="#ff0000"
    @hello="log">
    Apple
  </mybtn>
</template>

<script>
import MyBtn from '~/components/MyBtn'
export default {
  components: {
    MyBtn
  },
  methods: {
    log() {
      console.log('Hello world!')
    }
  }
}
</script>