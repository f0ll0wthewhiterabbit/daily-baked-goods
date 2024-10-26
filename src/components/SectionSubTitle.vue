<script setup lang="ts">
defineProps({
  text: { type: String, required: true },
})
</script>

<template>
  <h2 class="section-sub-title">{{ text }}</h2>
</template>

<style lang="scss" scoped>
.section-sub-title {
  font-family: 'Cormorant Garamond', serif;
  font-weight: 600;
  line-height: 1.2;
  color: var(--accent-color);
  display: flex;
  align-items: center;
  justify-content: center;
  width: max-content;
  height: 26px;

  &::before,
  &::after {
    width: 16px;
    height: 1px;
    background-color: var(--accent-color);
    display: block;
    content: '';
  }

  &::before {
    margin-right: 12px;
  }

  &::after {
    margin-left: 12px;
  }
}
</style>
