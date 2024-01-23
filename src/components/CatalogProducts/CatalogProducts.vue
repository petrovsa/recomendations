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

<style lang="scss">

.catalog {
    width: auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: auto;
    row-gap: 20px;
    margin-bottom: 20px;

    @media screen and (min-width: 768px) {
        max-width: 1700px;
        grid-template-columns: 1fr 1fr 1fr 1fr;       
    }

    .product-item {
      position: relative;
      max-width: 254px; 
    }
}
</style>