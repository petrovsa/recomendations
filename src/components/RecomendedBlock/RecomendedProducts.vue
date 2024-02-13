<template>
    <div v-for="(product, idx) in recomendedList" :key="idx" class="recomended-products" >
        <ProductsItem :book="product" />
    </div>
</template>

<script>
import ProductsItem from '@/components/ProductsItem/ProductsItem.vue';
export default {
    name: 'RecomendedProducts',

    props: {
        recomendedList: {
            type: Array,
            default: () => []
        }
    },

    components: {
        ProductsItem
    }
}
</script>

<style src="./RecomendedProducts.scss" lang="scss" />