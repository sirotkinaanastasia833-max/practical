<template>
    <div class="products-grid">
        <Product 
            v-for="product in products" 
            :key="product.id"
            v-bind="product"
        />
    </div>
</template>

<script setup lang="ts">
import Product from '@/components/ui/Product.vue'

interface ProductType {
    id: number
    title: string
    price: string
    size: string
    image: string
}

const products: ProductType[] = [
    { id: 1, title: 'Кулинарная гладь', price: '13', size: '180', image: '/src/assets/images/grey.png' },
    { id: 2, title: 'Кулинарная гладь', price: '122,4', size: '180', image: '/src/assets/images/orange.png' },
    { id: 3, title: 'Кулинарная гладь', price: '13,84', size: '180', image: '/src/assets/images/green.png' },
    { id: 4, title: 'Кулинарная гладь', price: '11,4', size: '180', image: '/src/assets/images/blue.png' },
    { id: 5, title: 'Кулинарная гладь', price: '13', size: '180', image: '/src/assets/images/grey.png' },
    { id: 6, title: 'Кулинарная гладь', price: '122,4', size: '180', image: '/src/assets/images/orange.png' },
    { id: 7, title: 'Кулинарная гладь', price: '13', size: '180', image: '/src/assets/images/grey.png' },
    { id: 8, title: 'Кулинарная гладь', price: '122,4', size: '180', image: '/src/assets/images/orange.png' },
    { id: 9, title: 'Кулинарная гладь', price: '13,84', size: '180', image: '/src/assets/images/green.png' },
    { id: 10, title: 'Кулинарная гладь', price: '11,4', size: '180', image: '/src/assets/images/blue.png' },
    { id: 11, title: 'Кулинарная гладь', price: '13', size: '180', image: '/src/assets/images/grey.png' },
    { id: 12, title: 'Кулинарная гладь', price: '122,4', size: '180', image: '/src/assets/images/orange.png' }
]
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
.products-grid {
    display: grid;
    grid-template-columns: repeat(3, auto);
    justify-content: end;
    gap: 40px 40px;
    padding-top: 20px;
    @include tablet{
        display: grid;
        grid-template-columns: repeat(2, auto);
    }
    @include mobile{
        display: grid;
        grid-template-columns: repeat(1, auto);
    }
}
</style>