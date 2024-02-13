<template>
  <div class="rating">
    <div class="rating__starslist">
      <div class="rating-star" v-for="idx in 5" :key="idx">
        <BaseIcon :name="`${stars >= idx ? 'star' : 'star-grey'}`" />
      </div>
    </div>
    <div class="rating__value">{{ rating }}</div>
  </div>
</template>

<script>
import BaseIcon from '@/components/BaseIcon/BaseIcon.vue';

export default {
  name: 'RatingElement',

  props: {
    rating: {
      type: Number,
      default: 0,
    },

    stars: {
      type: Number,
      default: null
    }
  },

  components: {BaseIcon}
}
</script>

<style lang="scss" src="./RatingElement.scss"/>