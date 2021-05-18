<template>
  <!-- key와 value가 같으면 key만 적어도 된다. 
    ex) color: color  ==> color -->

  <h1
    :style="[fontStyle, backgroundStyle]"
    @click="changeStyle">
    Hello?!
  </h1>
</template>

<script>
export default {
  data() {
    return {
      fontStyle: {
        color: 'orange',
        fontSize: '30px'
      },
      backgroundStyle: {
        backgroundColor: 'gray'
      }
    }
  },
  methods: {
    changeStyle() {
      this.fontStyle.color = 'royalblue'
      this.fontStyle.fontSize = '100px'
    }
  }
}
</script>