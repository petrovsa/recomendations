<template>
  <div class="slider">
    <div class="slider__header">
      <h2 class="slider__title"> {{ sliderName }}</h2>
      <div class="slider__navarrows">
        <div class="arrow arrow--left">
          <img src="./../assets/Icon.png" alt="icon" />
        </div>
        <div class="arrow arrow--right">
          <img src="./../assets/Icon.png" alt="icon" />
        </div>
      </div>
    </div>
    <div class="slider__container">
      <RecomendedProducts :recomendedList="listItems" />
    </div>
  </div>
</template>
<script>
import RecomendedProducts from './RecomendedBlock/RecomendedProducts.vue';

export default {
    name: 'SliderBooking',

    props: {
      listItems: {
        type: Array,
        default: () => {}
      },

      sliderName: {
        type: String,
        default: ''
      }
    },

    components: {
      RecomendedProducts
    }
    }
</script>

<style lang="scss" src="./SliderBooking.scss" />