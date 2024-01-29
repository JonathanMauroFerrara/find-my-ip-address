<script setup lang="ts">
import { toRefs } from 'vue'
const props = defineProps({
  title: { type: String, required: true },
  content: { type: String },
  customStyle: { type: String, default: '' }
})

const { title, content, customStyle } = toRefs(props)
</script>

<template>
  <div :class="customStyle" class="infobox">
    <div class="infobox__title">{{ title }}</div>
    <div class="infobox__content">
      <span>{{ content }}</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.infobox {
  &__title {
    text-align: center;
    font-size: 14px;
    font-weight: 700;
    color: #959595;
    margin-bottom: 10px;
    text-transform: uppercase;
    @media screen and (min-width: 768px) {
      text-align: left;
    }
  }
  &__content {
    text-align: center;
    font-size: 32px;
    font-weight: 700;
    color: black;
    overflow-wrap: break-word;
    @media screen and (min-width: 768px) {
      text-align: left;
    }
  }
}
</style>
