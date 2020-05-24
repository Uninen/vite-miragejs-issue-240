<script lang="ts">
import { defineComponent, ref } from 'vue'

import { Server } from 'miragejs'

new Server()

export default defineComponent({
  name: 'Home',
  async setup() {
    const count = ref(0)
    const inc = () => {
      count.value++
    }

    return {
      count,
      inc,
    }
  },
})
</script>
<template>
  <h1>Vite MirageJS Bug</h1>
  <button @click="inc">count is: {{ count }}</button>
</template>
