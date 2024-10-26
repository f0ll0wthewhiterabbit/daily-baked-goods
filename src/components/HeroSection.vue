<script setup lang="ts">
import { SECTION_IDS } from '../constants/navigation.constants'
import Header from './Header.vue'
import ArrowSvg from './icons/ArrowSvg.vue'
import SectionSubTitle from './SectionSubTitle.vue'
</script>

<template>
  <section class="hero-section">
    <Header />
    <div class="hero-section__content">
      <SectionSubTitle class="hero-section__sub-title" text="bonjour" />
      <h1 class="hero-section__title">
        Serving Baked Goods <span class="hero-section__bold-text">Every Day</span>
      </h1>
      <p class="hero-section__paragraph">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
        labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
        laboris nisi ut aliquip ex ea commodo consequat.
      </p>
      <a class="hero-section__link" :href="`#${SECTION_IDS.PRODUCTS}`">
        Shop Now <ArrowSvg class="hero-section__link-icon" />
      </a>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.hero-section {
  height: 1000px;
  background: url('../assets/images/hero-background.jpg') no-repeat center / cover;

  &__content {
    width: 716px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    margin: 175px auto 0;
    text-align: center;
  }

  &__sub-title {
    margin: 0 0 8px;
  }

  &__title {
    font-family: 'Cormorant Garamond', serif;
    font-weight: 600;
    font-size: 96px;
    letter-spacing: -3.36px;
    margin: 0 0 32px;
  }

  &__bold-text {
    font-weight: 700;
  }

  &__paragraph {
    font-family: 'Jost', sans-serif;
    font-weight: 400;
    font-size: 20px;
    line-height: 1.4;
    margin: 0 0 32px;
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
