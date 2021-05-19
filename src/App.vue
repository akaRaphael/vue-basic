<template>
  <button @click="handler">
    Click me!!!
  </button>
  <ul>
    <li
      v-for="{id, name} in newFruits"
      :key="id">
      {{ id }} = {{ name }}
    </li>
  </ul>
</template>

<script>
import shortid from 'shortid'
export default {
  data() {
    return {
      fruits: ['Apple', 'Banana', 'Cherry'],
    }
  },
  computed: {
    newFruits() {
      return this.fruits.map(fruit => ({
        id: shortid.generate(), // generate() => shortid를 생성해주는 메소드
        name: fruit
      }))
    }
  },
  methods: {
    handler() {
      this.fruits.push('Orange')
    }
  }
}
</script>

<style>
  button, li {
    font-size: 50px;
  }
</style>