<template>
    <div class="catalog">
        <ProductsItem :book="product"  v-for="(product, idx) in productsList" :key="idx" />
    </div>
</template>

<script>
import ProductsItem from '@/components/ProductsItem/ProductsItem.vue';

export default {
    name: 'CatalogProduts',

    props: {
        productsList: {
            type: Array,
            default: () => []
        }
    },

    components: {
        ProductsItem
    }
    }
</script>

<style lang="scss" src="./CatalogProducts.scss" />