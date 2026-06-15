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

<script>
import Product from '@/components/ui/Product.vue'

export default {
    components: {
        Product
    },
    data() {
        return {
            currentIndex: 0,
            productsPage1: [
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
            ],
            productsPage2: [
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
            ]
        }
    },
    methods: {
        nextSlide() {
            this.currentIndex = this.currentIndex === 0 ? 1 : 0
        },
        prevSlide() {
            this.currentIndex = this.currentIndex === 0 ? 1 : 0
        }
    }
}
</script>

<style scoped>
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
}

.arrow:hover {
    background-color: var(--dark-gold);
    transform: scale(1.1);
}

.arrow img {
    margin: 12px 0px 0px 12px;
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

.product-block{
    width: 100%;
    height: 650px;
    background-color: var(--saka-color);
}
</style>