<template>
    <div>
        <h2>Страница каталога</h2>
        <div class="content">
            <ProductItem 
            v-for="product in products" 
            :key="product.id" 
            :product="product" />
        </div>
    </div>
</template>

<script>
import { reactive } from 'vue'
import ProductItem from './ProductItem.vue';

export default {
    components: {
        ProductItem,
    },
    setup () {
        const products = reactive([
            {id: 1, name: 'Product 1', price: 100, desc: 'Description product 1'},
            {id: 2, name: 'Product 2', price: 200, desc: 'Description product 2'},
            {id: 3, name: 'Product 3', price: 300, desc: 'Description product 3'},
            {id: 4, name: 'Product 4', price: 500, desc: 'Description product 4'},
            {id: 5, name: 'Product 5', price: 600, desc: 'Description product 5'},
            {id: 6, name: 'Product 6', price: 700, desc: 'Description product 6'},

        ])
    
        return {
            products
        }
    }
}
</script>

<style lang="scss" scoped>
.content {
    display: flex;
    flex-wrap: wrap;
    gap: 32px;
    justify-content: center;
}
</style>