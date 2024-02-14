<template>
  <nav :class="['menu', classes]">
    <div
      v-for="(item, index) in props.data"
      :key="index"
      class="menu__item"
    >
      <a :href="item.route" class="menu__link">{{ item.label }}</a>
    </div>
  </nav>
</template>

<script setup>
import { computed } from 'vue';

// eslint-disable-next-line no-undef
const props = defineProps({
  data: Object,
  variant: String
})

const classes = computed(() => {
  return [
    props.variant ? `menu--${props.variant}` : ''
  ];
});

</script>

<style lang="scss" src="./TheMenu.scss" />
