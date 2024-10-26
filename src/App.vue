<script setup lang="ts">
import { provide, ref } from 'vue'
import HeroSection from './components/HeroSection.vue'
import InfoSection from './components/InfoSection.vue'
import OrderButton from './components/OrderButton.vue'
import ProductsSection from './components/ProductsSection.vue'

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
