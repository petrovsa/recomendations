<template>
    <a class="product-item" href="#">
        <img v-if="book.label" class="product-item__label" :src="book.label.url" alt="" />
        <button :class="['btn', 'product-item__wishlist', { 'in-wishlist': book.inWishlist }]" />
        <button class="btn product-item__cart" />
        <div class="product-item__picture">
            <img class="product-item__img" :src="book.imgUrl" alt="" />
        </div>
        <div class="product-item__text">
            <div class="product-item__name">
                {{ book.name }}
            </div>
            <a :href="book.autor.autorUrl" class="product-item__link">
                <div class="product-item__autor">
                    {{ book.autor.autor }}
                </div>
            </a>
          <RatingElement :stars="book.stars" :rating="book.ratingLabel" />
<!--            <RatingElement :stars="book.stars" :rating="book.ratingLabel" />-->
        </div>
        <div class="product-item__actions">
            <div class="product-item__price">
                <div :class="['product-item__price-item', { 'new': book.oldPrice }]">
                    <span class="product-item__price-normal">{{ book.price }}</span>
                    <span class="product-item__curency-normal">₴</span>
                </div>
                <div v-if="book.oldPrice" class="product-item__price-item">
                    <span class="product-item__price-old">{{ book.oldPrice }}</span>
                    <span class="product-item__curency-old">₴</span>
                </div>
            </div>
            <div v-if="book.inStock" class="product-item__status">
                В наявності
            </div>
            <div v-else class="product-item__status product-item__status--outstock">
                Немає в наявності
            </div>
        </div>
    </a>
</template>

<script>
import RatingElement from '../RatingElement/RatingElement.vue';

export default {
    name: 'ProductsItem',

    props: {
        book: {
            type: Object,
            default: () => { }
        }
    },

    components: {
        RatingElement,
    }
}
</script>

<style lang="scss" src="./ProductsItem.scss" />