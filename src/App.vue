<script setup lang="ts">
import { CartProvider } from './features/cart/'
import { HeroSection } from './features/hero'
import { InfoSection } from './features/info'
import { ProductsSection } from './features/products'
import { OrderButton } from './common'
</script>

<template>
  <CartProvider>
    <HeroSection />
    <InfoSection />
    <ProductsSection />
    <OrderButton />
  </CartProvider>
</template>
