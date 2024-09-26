<template>
    <div class="product">
        <h3>{{ product.name }}</h3>
        <p>{{ product.desc }}</p>
        <p>{{ product.price }}</p>
        <Counter />
        <button>Купить</button>
    </div>
</template>

<script>
import Counter from '../components/Counter.vue'
export default {
    components: {
        Counter
    },
    props: {
        product: {
            type: Object,
            required: true
        }
    }
}
</script>

<style lang="scss" scoped>
.product {
    text-align: left;
    border: 1px solid black;
    border-radius: 15px;
    padding: 8px 24px;
}
</style>