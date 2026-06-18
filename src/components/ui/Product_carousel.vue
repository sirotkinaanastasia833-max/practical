<template>
    <div class="product-block">
        <Container><h3>Недавно просмотренные</h3></Container>
        <div class="products">
            <div class="arrow left" @click="prevSlide">
                <img src="./../../assets/images/ArrowLeft.png" alt="">
            </div>
            
            <div class="products-wrapper">
                <div class="products-track" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
                    <div class="products-page" v-for="(page, index) in pages" :key="index">
                        <Product 
                            v-for="(product, idx) in page" 
                            :key="idx"
                            :title="product.title"
                            :price="product.price"
                            :size="product.size"
                            :image="product.image"
                            class="product-item"
                        />
                    </div>
                </div>
            </div>
            
            <div class="arrow right" @click="nextSlide">
                <img src="./../../assets/images/ArrowRight.png" alt="">
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'
import Product from '@/components/ui/Product.vue'
import Container from '../layout/Container.vue'

interface ProductItem {
    title: string
    price: string | number
    size: string | number
    image: string
}

const currentIndex = ref<number>(0)

const allProducts = ref<ProductItem[]>([
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
    },
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
const pages = computed(() => {
    const itemsPerPage = 4
    const result: ProductItem[][] = []
    for (let i = 0; i < allProducts.value.length; i += itemsPerPage) {
        result.push(allProducts.value.slice(i, i + itemsPerPage))
    }
    return result
})
const totalPages = computed(() => pages.value.length)
const nextSlide = (): void => {
    currentIndex.value = (currentIndex.value + 1) % totalPages.value
}
const prevSlide = (): void => {
    currentIndex.value = (currentIndex.value - 1 + totalPages.value) % totalPages.value
}
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;

.product-block {
    width: 100%;
    height: 660px;
    background-color: var(--saka-color);

    @include tablet {
        height: auto;
        padding-bottom: 40px;
    }

    @include mobile {
        height: auto;
        padding-bottom: 30px;
    }
}

h3 {
    font-size: var(--text-2xl);
    font-family: var(--font-family);
    margin: 60px 0px 0px 170px;
    font-weight: 500;
    padding-top: 70px;
    padding-bottom: 30px;

    @include tablet {
        font-size: 24px;
        margin: 30px 0px 0px 30px;
        padding-top: 40px;
        padding-bottom: 20px;
    }

    @include mobile {
        font-size: 20px;
        margin: 20px 0px 0px 16px;
        padding-top: 30px;
        padding-bottom: 15px;
    }
}

.products {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 0 30px;

    @include tablet {
        padding: 0 30px;
        gap: 12px;
    }

    @include mobile {
        padding: 0 16px;
        gap: 8px;
    }
}

.arrow {
    background-color: white;
    border-radius: 50%;
    width: 50px;
    height: 50px;
    cursor: pointer;
    transition: all 0.3s ease;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;

    &:hover {
        background-color: var(--dark-gold);
        transform: scale(1.1);
    }

    img {
        width: 20px;
        height: 20px;
        margin: 0;
    }

    &.left img {
        transform: rotate(180deg);
    }

    @include tablet {
        width: 36px;
        height: 36px;

        img {
            width: 14px;
            height: 14px;
        }
    }

    @include mobile {
        width: 30px;
        height: 30px;

        img {
            width: 12px;
            height: 12px;
        }
    }
}

.products-wrapper {
    overflow: hidden;
    flex: 1;
}

.products-track {
    display: flex;
    transition: transform 0.5s ease;
}

.products-page {
    display: flex;
    flex-shrink: 0;
    width: 100%;
    justify-content: center;
    gap: 40px;

    @include tablet {
        gap: 20px;
        justify-content: center;
    }

    @include mobile {
        gap: 16px;
        justify-content: center;
    }
}

.product-item {
    width: 260px;
    height: 430px;
    flex-shrink: 0;

    @include tablet {
        width: 300px;
        height: 497px;
    }

    @include mobile {
        width: 300px;
        height: 497px;
    }
}

@include tablet {
    .product-item:nth-child(3),
    .product-item:nth-child(4) {
        display: none;
    }
}

@include mobile {
    .product-item:nth-child(2),
    .product-item:nth-child(3),
    .product-item:nth-child(4) {
        display: none;
    }
}
</style>