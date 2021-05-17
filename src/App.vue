<template>
  <h1
    @[event]="add"
    :[attr]="'active'">
    {{ msg }}
  </h1>
</template>

<script>
export default {
  data() {
    return {
      msg: 'active',
      attr: 'class',
      event: 'click'
    }
  },
  methods: {
    add() {
      this.msg += '!'
    }
  }  
}
</script>

<style lang="scss">

  .active {
    color: royalblue;
    font-size: 100px;
  }

</style>