<template>
    <div class="product-block">
        <h3>Недавно просмотренные</h3>
        <div class="products">
            <div class="arrow" @click="prevSlide">
                <img src="./../../assets/images/ArrowLeft.png" alt="">
            </div>
            
            <div class="products-wrapper">
                <div class="products-track" :style="{ transform: 'translateX(-' + currentIndex * 100 + '%)' }">
                    <div class="products-page">
                        <Product 
                            v-for="(product, index) in productsPage1" 
                            :key="index"
                            :title="product.title"
                            :price="product.price"
                            :size="product.size"
                            :image="product.image"
                        />
                    </div>
                    <div class="products-page">
                        <Product 
                            v-for="(product, index) in productsPage2" 
                            :key="index"
                            :title="product.title"
                            :price="product.price"
                            :size="product.size"
                            :image="product.image"
                        />
                    </div>
                </div>
            </div>
            
            <div class="arrow" @click="nextSlide">
                <img src="./../../assets/images/ArrowRight.png" alt="">
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Product from '@/components/ui/Product.vue'

interface ProductItem {
    title: string
    price: string | number
    size: string | number
    image: string
}

const currentIndex = ref<number>(0)

const productsPage1 = ref<ProductItem[]>([
    {
        title: 'Кулинарная гладь',
        price: '11,4',
        size: '180',
        image: '/src/assets/images/blue.png'
    },
    {
        title: 'Кулинарная гладь',
        price: '13',
        size: '180',
        image: '/src/assets/images/grey.png'
    },
    {
        title: 'Кулинарная гладь',
        price: '122,4',
        size: '180',
        image: '/src/assets/images/orange.png'
    },
    {
        title: 'Кулинарная гладь',
        price: '13,84',
        size: '180',
        image: '/src/assets/images/green.png'
    }
])

const productsPage2 = ref<ProductItem[]>([
    {
        title: 'Кулинарная гладь',
        price: '11,4',
        size: '180',
        image: '/src/assets/images/blue.png'
    },
    {
        title: 'Кулинарная гладь',
        price: '13',
        size: '180',
        image: '/src/assets/images/grey.png'
    },
    {
        title: 'Кулинарная гладь',
        price: '122,4',
        size: '180',
        image: '/src/assets/images/orange.png'
    },
    {
        title: 'Кулинарная гладь',
        price: '13,84',
        size: '180',
        image: '/src/assets/images/green.png'
    }
])

const nextSlide = (): void => {
    currentIndex.value = currentIndex.value === 0 ? 1 : 0
}

const prevSlide = (): void => {
    currentIndex.value = currentIndex.value === 0 ? 1 : 0
}
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;

.product-block {
    width: 100%;
    height: 650px;
    background-color: var(--saka-color);
}

h3 {
    font-size: var(--text-2xl);
    font-family: var(--font-family);
    margin: 60px 0px 0px 170px;
    font-weight: 500;
    padding-top: 70px;
    padding-bottom: 30px;
}

.arrow {
    background-color: white;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    cursor: pointer;
    transition: all 0.3s ease;
    flex-shrink: 0;
    margin-top: 220px;

    &:hover {
        background-color: var(--dark-gold);
        transform: scale(1.1);
    }

    img {
        margin: 12px 0px 0px 12px;
    }
}

.products {
    display: flex;
    flex-wrap: nowrap;
    margin-left: 60px;
    margin-right: 60px;
    align-items: flex-start;
    gap: 20px;
}

.products-wrapper {
    overflow: hidden;
    flex: 1;
}

.products-track {
    display: flex;
    transition: transform 0.4s ease;
}

.products-page {
    display: flex;
    flex-shrink: 0;
    width: 100%;
    justify-content: center;
    gap: 40px;
}
</style>