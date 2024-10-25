<script setup lang="ts">
import { ref } from 'vue'
import BasketSvg from './icons/BasketSvg.vue'

const itemsInBasket = ref<number>(8)
</script>

<template>
  <button class="basket-button" type="button">
    <BasketSvg class="basket-button__icon" />
    <div class="basket-button__counter">{{ itemsInBasket }}</div>
  </button>
</template>

<style lang="scss" scoped>
.basket-button {
  width: 44px;
  height: 44px;
  background-color: #fff;
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  cursor: pointer;

  &__icon {
    color: #231f20;
    width: 20px;
    height: 20px;
  }

  &__counter {
    position: absolute;
    top: 0;
    right: 0;
    border-radius: 50%;
    background-color: #231f20;
    font-family: 'Lusitana', serif;
    font-weight: 700;
    font-size: 16px;
    line-height: 1.8;
    letter-spacing: -0.56px;
    color: #fff;
    width: 24px;
    height: 24px;
    transform: translate(50%, -50%);
    display: flex;
    align-items: center;
    justify-content: center;
  }
}
</style>
