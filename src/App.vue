<script setup lang="ts">
import { provide, ref } from 'vue'
import { HeroSection } from './features/hero'
import { InfoSection } from './features/info'
import { ProductsSection } from './features/products'
import { OrderButton } from './common'

const itemsInCart = ref<number>(0)

function addToCart(): void {
  itemsInCart.value += 1
}

provide('itemsInCart', itemsInCart)
provide('addToCart', addToCart)
</script>

<template>
  <HeroSection />
  <InfoSection />
  <ProductsSection />
  <OrderButton />
</template>
