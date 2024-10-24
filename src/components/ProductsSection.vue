<script setup lang="ts">
import { PRODUCTS } from '../constants/product.constants'
import ProductCard from './ProductCard.vue'
</script>

<template>
  <section class="products-section">
    <ul class="products-section__list">
      <ProductCard
        v-for="product in PRODUCTS"
        class="products-section__card"
        :key="product.id"
        :product
      />
    </ul>
  </section>
</template>

<style lang="scss" scoped>
.products-section {
  padding: 96px 0;

  &__list {
    display: flex;
    align-items: center;
    gap: 32px;
    margin: 0 auto;
    padding: 0 64px;
    list-style: none;
    width: max-content;
  }

  &__card {
    flex-shrink: 0;
  }
}
</style>
