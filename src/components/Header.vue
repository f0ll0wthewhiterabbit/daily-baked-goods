<script setup lang="ts">
import BasketButton from './BasketButton.vue'
</script>

<template>
  <header class="header">
    <nav>
      <ul class="header__list">
        <li>
          <a class="header__link" href="#">Store</a>
        </li>
        <li>
          <a class="header__link" href="#">About</a>
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
    <BasketButton />
  </header>
</template>

<style lang="scss" scoped>
.header {
  height: 76px;

  padding: 0 96px 0 272px;
  display: flex;
  align-items: center;
  justify-content: space-between;

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
