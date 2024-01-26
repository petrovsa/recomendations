<template>
  <div class="slider">
    <div class="slider__header">
      <h2 class="slider__title"> {{ sliderName }}</h2>
      <div class="slider__nav">
        <div class="slider__arrow slider__arrow--left">
          <img src="../../assets/Icon.png" alt="icon" />
        </div>
        <div class="slider__arrow slider__arrow--right">
          <img src="../../assets/Icon.png" alt="icon" />
        </div>
      </div>
    </div>
    <div class="slider__container">
      <slot></slot>
    </div>
  </div>
</template>
<script>
export default {
    name: 'TheSlider',

    props: {
      sliderName: {
        type: String,
        default: ''
      }
    }
}
</script>

<style lang="scss" src="./TheSlider.scss" />