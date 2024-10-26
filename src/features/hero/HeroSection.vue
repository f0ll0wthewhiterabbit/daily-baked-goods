<script setup lang="ts">
import { SectionSubTitle } from '../../common'
import { SECTION_IDS } from '../../constants'
import { Header } from '../../common'
import ArrowSvg from './ArrowSvg.vue'
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
  background: url('../../assets/images/hero-background.jpg') no-repeat center / cover;

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
    line-height: 1;
    letter-spacing: -3.36px;
    margin: 0 0 32px;
  }

  &__bold-text {
    font-weight: 700;
  }

  &__paragraph {
    margin: 0 0 32px;
  }

  &__link {
    display: block;
    font-weight: 500;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    width: 196px;
    height: 60px;
    text-decoration: none;
    color: var(--text-color);
    border: 1px solid var(--accent-color);
    background-color: var(--accent-color-transparent);
    text-shadow: 2px 2px var(--color-white);

    &:visited {
      color: var(--text-color);
    }
  }

  &__link-icon {
    width: 27px;
    height: 14px;
    color: var(--accent-color);
  }
}
</style>
