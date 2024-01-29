<script setup lang="ts">
import { toRefs } from 'vue'
const props = defineProps({
  title: { type: String, required: true },
  content: { type: String }
})

const { title, content } = toRefs(props)
</script>

<template>
  <div class="box">
    <div class="box__title">{{ title }}</div>
    <div class="box__content">
      <span></span>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
