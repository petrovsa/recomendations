<template>
    <div class="rating">
        <div class="rating__starslist">
            <div class="rating-star">
                <img src="./../../assets/star.jpg" alt="star" />
            </div>
            <div class="rating-star">
                <img src="./../../assets/star.jpg" alt="star" />
            </div>
            <div class="rating-star">
                <img src="./../../assets/star.jpg" alt="star" />
            </div>
            <div class="rating-star">
                <img src="./../../assets/star.jpg" alt="star" />
            </div>
            <div class="rating-star">
                <img src="./../../assets/star.jpg" alt="star" />
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
        }
    }
    }
</script>

<style lang="scss" src="./RatingElement.scss" />