<template>
  <div class="rating">
    <div class="rating__starslist">
      <div class="rating-star" v-for="idx in 5" :key="idx">
        <img :src="require(`@/assets/star${stars >= idx ? '' : '-grey'}.svg`)" alt="star"/>
      </div>
    </div>
    <div class="rating__value">{{ rating }}</div>
  </div>
</template>

<script>
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
  }
}
</script>

<style lang="scss" src="./RatingElement.scss"/>