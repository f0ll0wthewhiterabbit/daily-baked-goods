<script setup lang="ts">
import CartButton from './CartButton.vue'
import { SECTION_IDS } from '../constants/navigation.constants'
</script>

<template>
  <header class="header">
    <a class="header__logo" href="#" aria-label="Daily Baked Goods">
      <img src="../assets/images/logo.jpg" alt="Daily Baked Goods" />
    </a>
    <nav>
      <ul class="header__list">
        <li>
          <a class="header__link" :href="`#${SECTION_IDS.PRODUCTS}`">Store</a>
        </li>
        <li>
          <a class="header__link" :href="`#${SECTION_IDS.INFO}`">About</a>
        </li>
        <li>
          <a class="header__link" href="#">Shipping</a>
        </li>
        <li>
          <a class="header__link" href="#">Recipes</a>
        </li>
        <li>
          <a class="header__link" href="#">Blog</a>
        </li>
      </ul>
    </nav>
    <CartButton />
  </header>
</template>

<style lang="scss" scoped>
.header {
  height: 76px;
  position: relative;
  padding: 0 96px 0 272px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  &__logo {
    display: block;
    width: 128px;
    height: 127px;
    text-decoration: none;
    position: absolute;
    top: 0;
    left: 64px;
  }

  &__list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    align-items: center;
    gap: 48px;
  }

  &__link {
    font-size: 20px;
    line-height: 1.4;
    color: #231f20;
    letter-spacing: -0.7px;
    text-decoration: none;
    font-family: 'Lusitana', serif;
    font-weight: 400;

    &:visited {
      color: #231f20;
    }
  }
}
</style>
