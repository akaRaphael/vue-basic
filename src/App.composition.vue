<template>
  <h1 @click="increase">
    {{ count }} / {{ doubleCount }}
  </h1>
  <h1 @click="changeMessage">
    {{ message }} / {{ reversedMessage }}
  </h1>
</template>
<script>
import {ref, computed, watch, onMounted} from 'vue'
export default {
  setup() { 
    // setup() 메소드의 실행 시점은 created와 동일하다. 
    // 그러므로 created 라이프 사이클은 따로 존재하지 않는다.
    console.log('setup = ', message.value)

    // count 관련
    let count = ref(0)
    const doubleCount = computed(() => {
      return count.value * 2
    })
    function increase() {
      count.value += 1
    }

    // message 관련 
    let message = ref('Hello world?')
    const reversedMessage = computed(() => {
      return message.value.split('').reverse().join('')
    })
    watch(message, (newValue) => {
      console.log(newValue)
    })
    function changeMessage() {
      message.value = 'How are you?'
    }

    onMounted(() => {
      console.log('onMounted = ', count.value)
    })

    return {
      count,
      increase,
      doubleCount,
      message,
      reversedMessage,
      changeMessage
    }

  }
}
</script>