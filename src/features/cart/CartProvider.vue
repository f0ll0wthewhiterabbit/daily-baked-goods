<template>
  <slot />
</template>

<script setup lang="ts">
import { provide, ref } from 'vue'

const itemsInCart = ref<number>(0)

function addToCart(): void {
  itemsInCart.value += 1
}

provide('itemsInCart', itemsInCart)
provide('addToCart', addToCart)
</script>
