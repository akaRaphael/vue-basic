<template>
  <div
    v-bind="$attrs" 
    class="btn"
    @click="hello">
    <slot></slot>
  </div>
</template>

<script>
import {onMounted} from 'vue'
export default {
  inheritAttrs: false,
  props: {
    color: {
      type: String,
      default: 'gray'
    }
  },
  emits: ['hello'],
  setup(props, context) {
    function hello(context) {
      context.emit('hello') 
    }
    onMounted(() => {
      console.log('props = ', props)
      console.log('context = ',context)

      console.log(props.color)// this.color로 접근이 불가하여 props를 통해 접근
      console.log(context.attrs)// this.$attrs로 접근이 불가하여 context를 통해 접근

    })

    return {
      hello
    }
  }
}
</script>