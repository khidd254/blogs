<template>
  <div class="home">
   home
   <p ref="p">My name is {{ name }}</p>
   <p>I am {{ age }} years old</p>
   <button @click="handleClick">click me</button>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'HomeView',
  setup() {
    console.log('setup')

    const p = ref(null)

    let name = 'Ken'
    let age = 30

    const handleClick = () => {
      console.log(p)
    }

    return {name, age, handleClick, p}

  }
}
</script>
