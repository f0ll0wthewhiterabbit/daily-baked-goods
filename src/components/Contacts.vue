<script setup lang="ts">
import FacebookSvg from './icons/FacebookSvg.vue'
import InstagramSvg from './icons/InstagramSvg.vue'

// TODO:
</script>

<template>
  <div class="contacts">
    <h3 class="contacts__title">Follow Us</h3>
    <ul class="contacts__list">
      <li class="contacts__item">
        <a class="contacts__link" href="#">
          <FacebookSvg class="contacts__icon" />
        </a>
      </li>
      <li class="contacts__item">
        <a class="contacts__link" href="#">
          <InstagramSvg class="contacts__icon" />
        </a>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.contacts {
  height: 28px;
  display: flex;
  align-items: center;
  justify-content: space-between;

  &__title {
    font-family: 'Jost', sans-serif;
    font-weight: 500;
    font-size: 20px;
    line-height: 1.2;
    color: #231f20;
    margin: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 24px;
    margin-right: 24px;

    &::after {
      content: '';
      width: 80px;
      height: 1px;
      background-color: #cf8c0b;
      display: block;
    }
  }

  &__list {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 16px;
    margin: 0;
    padding: 0;
    list-style: none;
  }

  &__link {
    text-decoration: none;
    color: #231f20;

    &:visited {
      color: #231f20;
    }
  }

  &__icon {
    width: 24px;
    height: 24px;
  }
}
</style>
