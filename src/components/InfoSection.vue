<script setup lang="ts">
import { SECTION_IDS } from '../constants/navigation.constants'
import Contacts from './Contacts.vue'
import SectionSubTitle from './SectionSubTitle.vue'
</script>

<template>
  <section class="info-section" :id="SECTION_IDS.INFO">
    <div class="info-section__content">
      <SectionSubTitle class="info-section__sub-title" text="patisserie" />
      <h1 class="info-section__title">Lorem Ipsum</h1>
      <p class="info-section__paragraph">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
        labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
        laboris nisi ut aliquip ex ea commodo consequat.
      </p>
      <p class="info-section__paragraph">
        Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
        pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>
      <Contacts />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.info-section {
  padding: 192px 0 96px;

  &__content {
    width: 720px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    margin: 0 auto;
    text-align: center;
  }

  &__sub-title {
    margin: 0 0 8px;
  }

  &__title {
    font-family: 'Cormorant Garamond', serif;
    font-weight: 700;
    font-size: 96px;
    letter-spacing: -3.36px;
    margin: 0 0 24px;
  }

  &__bold-text {
    font-weight: 700;
  }

  &__paragraph {
    font-family: 'Jost', sans-serif;
    font-weight: 400;
    font-size: 20px;
    line-height: 1.4;
    margin: 0 0 24px;

    &:last-of-type {
      margin-bottom: 40px;
    }
  }

  &__link {
    display: block;
    font-family: 'Jost', sans-serif;
    font-weight: 500;
    font-size: 20px;
    line-height: 1.4;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    width: 196px;
    height: 60px;
    text-decoration: none;
    color: #231f20;
    border: 1px solid #cf8c0b;
    background-color: #cf8c0b1a;
    text-shadow: 2px 2px #fff;

    &:visited {
      color: #231f20;
    }
  }

  &__link-icon {
    width: 27px;
    height: 14px;
    color: #cf8c0b;
  }
}
</style>
