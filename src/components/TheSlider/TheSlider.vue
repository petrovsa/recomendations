<template>
  <div class="slider">
    <div class="slider__header">
      <h2 class="slider__title"> {{ sliderName }}</h2>
      <div class="slider__nav">
        <div class="slider__arrow slider__arrow--left">
          <BaseIcon name="arrow" />
        </div>
        <div class="slider__arrow slider__arrow--right">
          <BaseIcon name="arrow" />
        </div>
      </div>
    </div>
    <div class="slider__container">
      <slot></slot>
    </div>
  </div>
</template>
<script>
import BaseIcon from '@/components/BaseIcon/BaseIcon.vue';

export default {
    name: 'TheSlider',

    props: {
      sliderName: {
        type: String,
        default: ''
      }
    },

    components: {BaseIcon}
}
</script>

<style lang="scss" src="./TheSlider.scss" />