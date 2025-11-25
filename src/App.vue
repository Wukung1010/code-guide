<script lang="ts" setup>
import { ref, computed } from 'vue'
import Button from './components/Button.vue'

const themePrefix = 'myapp'

const themeObj = ref({
  fontColor: '#dddddd',
})
const themeStr = computed(() => {
  let str = ''

  Object.entries(themeObj.value).forEach(([key, value]) => {
    const CSSKey = `--${themePrefix}-${key.replace(/([A-Z])/g, '-$1').toLowerCase()}`
    str += `${CSSKey}: ${value}; `
  })

  return str
})
</script>

<template>
  <div :style="themeStr">
    <Button>按钮</Button>
  </div>
</template>

<style>
.button {
  color: var(--myapp-font-color);
}
</style>
