<script setup lang="ts">
import { computed, PropType, ref } from 'vue'
import ChevronSvg from './icons/ChevronSvg.vue'
import MinusSvg from './icons/MinusSvg.vue'
import PlusSvg from './icons/PlusSvg.vue'
import { Product } from '../interfaces/product.interface'

const props = defineProps({
  product: { type: Object as PropType<Product>, required: true },
})

const quantity = ref<number>(5)
const pack = ref<number>(props.product.availablePacks[0])

const price = computed<number>(() => props.product.price * quantity.value * pack.value)

function getImageUrl(imageName: string): string {
  return new URL(`../assets/images/${imageName}`, import.meta.url).href
}
</script>

<template>
  <li class="product-card">
    <div class="product-card__image-wrapper">
      <img class="product-card__image" :src="getImageUrl(product.image)" alt="Product image" />
    </div>
    <h3 class="product-card__title">{{ product.name }}</h3>
    <h3 class="product-card__paragraph">{{ product.description }}</h3>
    <footer class="product-card__footer">
      <div class="product-card__select-wrapper">
        <select class="product-card__select" v-model="pack">
          <option v-for="size in product.availablePacks" :key="size" :value="size">
            Pack of {{ size }}
          </option>
        </select>
        <ChevronSvg class="product-card__select-icon" />
      </div>
      <div class="product-card__quantity-selector">
        <button
          class="product-card__quantity-button"
          type="button"
          @click="quantity -= 1"
          :disabled="quantity === 0"
        >
          <MinusSvg class="product-card__quantity-icon" />
        </button>
        <span class="product-card__quantity">{{ quantity }}</span>
        <button class="product-card__quantity-button" type="button" @click="quantity += 1">
          <PlusSvg class="product-card__quantity-icon" />
        </button>
      </div>
      <span class="product-card__price">${{ price }}</span>
      <button class="product-card__add-button" type="button">
        <PlusSvg class="product-card__add-icon" />
        Add To Cart
      </button>
    </footer>
  </li>
</template>

<style lang="scss" scoped>
.product-card {
  width: 480px;

  &__image-wrapper {
    background-color: #f9efe0;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 64px;
    margin-bottom: 20px;
  }

  &__image {
    width: 352px;
    height: 322px;
  }

  &__title {
    font-family: 'Cormorant Garamond', serif;
    font-weight: 600;
    font-size: 24px;
    margin: 0 0 8px;
    letter-spacing: -0.84px;
    line-height: 1.2;
  }

  &__paragraph {
    font-family: 'Jost', sans-serif;
    font-weight: 400;
    font-size: 16px;
    line-height: 1.5;
    margin: 0 0 20px;
  }

  &__footer {
    display: grid;
    grid-template-columns: repeat(2, max-content) 1fr;
    gap: 10px 12px;
  }

  &__select-wrapper {
    position: relative;
  }

  &__select {
    height: 40px;
    padding: 8px 44px 8px 24px;
    background-color: #cf8c0b1a;
    border-radius: 64px;
    border: none;
    font-family: 'Jost', sans-serif;
    font-weight: 500;
    font-size: 18px;
    line-height: 1.333333;
    appearance: none;
    -webkit-appearance: none;
    -moz-appearance: none;
  }

  &__select-icon {
    position: absolute;
    top: 50%;
    right: 22px;
    width: 12px;
    height: 8px;
    color: #cf8c0b;
    transform: translateY(-50%);
    pointer-events: none;
  }

  &__quantity-selector {
    display: flex;
    align-items: center;
    gap: 16px;
    height: 40px;
    padding: 0 16px;
    background-color: #cf8c0b1a;
    border-radius: 64px;
  }

  &__quantity-button {
    background-color: transparent;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #cf8c0b;
    padding: 0;
    height: 24px;

    &:disabled {
      cursor: not-allowed;
    }
  }

  &__quantity-icon {
    width: 10px;
  }

  &__quantity,
  &__price,
  &__add-button {
    font-family: 'Jost', sans-serif;
    font-weight: 500;
    font-size: 18px;
    line-height: 1.333333;
  }

  &__price {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    height: 40px;
  }

  &__add-button {
    grid-column: 1 / -1;
    height: 56px;
    background-color: #cf8c0b1a;
    border: none;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 16px;
    cursor: pointer;
  }

  &__add-icon {
    color: #cf8c0b;
    width: 15px;
    height: 15px;
  }
}
</style>
