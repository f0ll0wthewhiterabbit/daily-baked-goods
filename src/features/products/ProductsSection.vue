<script setup lang="ts">
import { Swiper, SwiperSlide } from 'swiper/vue'
import { SECTION_IDS } from '../../constants'
import { PRODUCTS } from './product.constants'
import ProductCard from './ProductCard.vue'
</script>

<template>
  <section class="products-section" :id="SECTION_IDS.PRODUCTS">
    <Swiper
      class="products-section__list"
      role="list"
      aria-live="polite"
      :spaceBetween="32"
      slidesPerView="auto"
      grabCursor
    >
      <SwiperSlide
        class="products-section__slide"
        v-for="product in PRODUCTS"
        :key="product.id"
        role="listitem"
      >
        <ProductCard class="products-section__card" :product />
      </SwiperSlide>
    </Swiper>
  </section>
</template>

<style lang="scss" scoped>
.products-section {
  padding: 96px 0;
  overflow-x: hidden;

  &__list {
    margin: 0 auto;
    padding: 0 64px;
  }

  &__slide {
    width: max-content;
  }

  &__card {
    flex-shrink: 0;
  }
}
</style>
