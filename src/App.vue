<template>
  <MyBtn>Banana</MyBtn>
  <MyBtn 
    :color="color">
    Apple
  </MyBtn>
  <MyBtn 
    large
    color="salmon">
    Cherry
  </MyBtn>
  <MyBtn><span style="color: orange;">Mango</span></MyBtn>
</template>

<script>
import MyBtn from '~/components/MyBtn'
export default {
  components: {
    MyBtn
  },
  data() {
    return {
      color: 'royalblue'
    }
  }
}
</script> 