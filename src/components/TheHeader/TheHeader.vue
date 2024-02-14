<template>
  <header class="header">
    <div class="header__top">
      <div class="container header__top-container">
        <TheMenu :data="menuTop" variant="light" />
        <LangSwitcher />
      </div>
    </div>
    <div class="header__body">
      <div class="container header__body-container">
        <div class="header__action header__action--menu">
          <div class="header__action-icon">i</div>
        </div>
        <div class="header__logo">
          logo
        </div>
        <div class="header__catalog">
          <div class="header__catalog-icon">i</div>
          Каталог книг
        </div>
        <div class="header__search">
          search
        </div>
        <div class="header__action header__action--chat">
          <div class="header__action-icon">i</div>
          Чат рекомендації AI
        </div>
        <div class="header__row">
          <div class="header__action">
            <div class="header__action-icon">i</div>
          </div>
          <div class="header__action">
            <div class="header__action-icon">i</div>
          </div>
          <div class="header__action">
            <div class="header__action-icon">i</div>
          </div>
        </div>
      </div>
    </div>
    <div class="header__bottom">
      <div class="container header__bottom-container">
        <TheMenu :data="menuBottom" />
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';

import LangSwitcher from "@/components/LangSwitcher/LangSwitcher.vue";
import TheMenu from "@/components/TheMenu/TheMenu.vue";

const menuTop = ref([
  { label: 'Наші кафе-книгарні', route: '/' },
  { label: 'Автори', route: '/' },
  { label: 'Покупцям', route: '/' },
  { label: 'Як стати франчайзі', route: '/' },
  { label: 'Звʼязатися', route: '/' }
]);

const menuBottom = ref([
  { label: 'Новинки', route: '/' },
  { label: 'Лідери продажів', route: '/' },
  { label: 'Вибір читачів', route: '/' },
  { label: 'Найкращі книги місяця', route: '/' },
  { label: 'Найкращі книги 2023 року', route: '/' }
]);
</script>

<style lang="scss" src="./TheHeader.scss" />
