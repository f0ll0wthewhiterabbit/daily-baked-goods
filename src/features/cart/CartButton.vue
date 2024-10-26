<script setup lang="ts">
import CartSvg from './CartSvg.vue'
import { inject } from 'vue'

const itemsInCart = inject<number>('itemsInCart')
</script>

<template>
  <button class="cart-button" type="button" aria-label="Cart">
    <CartSvg class="cart-button__icon" />
    <div v-if="itemsInCart" class="cart-button__counter">{{ itemsInCart }}</div>
  </button>
</template>

<style lang="scss" scoped>
.cart-button {
  width: 44px;
  height: 44px;
  background-color: var(--color-white);
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  cursor: pointer;

  &::after {
    content: '';
    display: block;
    position: absolute;
    top: -2px;
    left: -2px;
    background-color: var(--color-white);
    width: 48px;
    height: 48px;
    clip-path: polygon(
      0px 0px,
      4px 0px,
      4px 2px,
      11px 2px,
      11px 0px,
      15px 0px,
      15px 2px,
      22px 2px,
      22px 0px,
      26px 0px,
      26px 2px,
      33px 2px,
      33px 0px,
      37px 0px,
      37px 2px,
      44px 2px,
      44px 0px,
      48px 0px,
      48px 4px,
      46px 4px,
      46px 11px,
      48px 11px,
      48px 15px,
      46px 15px,
      46px 22px,
      48px 22px,
      48px 26px,
      46px 26px,
      46px 33px,
      48px 33px,
      48px 37px,
      46px 37px,
      46px 44px,
      48px 44px,
      48px 48px,
      44px 48px,
      44px 46px,
      37px 46px,
      37px 48px,
      33px 48px,
      33px 46px,
      26px 46px,
      26px 48px,
      22px 48px,
      22px 46px,
      15px 46px,
      15px 48px,
      11px 48px,
      11px 46px,
      4px 46px,
      4px 48px,
      0px 48px,
      0px 44px,
      2px 44px,
      2px 37px,
      0px 37px,
      0px 33px,
      2px 33px,
      2px 26px,
      0px 26px,
      0px 22px,
      2px 22px,
      2px 15px,
      0px 15px,
      0px 11px,
      2px 11px,
      2px 4px,
      0px 4px
    );
  }

  &__icon {
    color: var(--text-color);
    width: 20px;
    height: 20px;
    z-index: 5;
  }

  &__counter {
    position: absolute;
    top: 0;
    right: 0;
    border-radius: 50%;
    background-color: var(--text-color);
    font-family: 'Lusitana', serif;
    font-weight: 700;
    font-size: 16px;
    line-height: 1.8;
    letter-spacing: -0.56px;
    color: var(--color-white);
    width: 24px;
    height: 24px;
    transform: translate(50%, -50%);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 10;
  }
}
</style>
