<script lang="ts">
import { defineComponent } from 'vue'

import Home from './components/Home.vue'

export default defineComponent({
  name: 'App',
  components: {
    Home,
  },
})
</script>

<template>
  <Suspense>
    <template #default>
      <home></home>
    </template>
    <template #fallback>
      Loading...
    </template>
  </Suspense>
</template>
