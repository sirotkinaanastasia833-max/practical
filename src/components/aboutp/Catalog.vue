<template>
    <div class="products-grid">
        <div class="products-row" v-for="(row, rowIndex) in productRows" :key="rowIndex">
            <Product 
                v-for="(product, colIndex) in row" 
                :key="colIndex"
                :title="product.title"
                :price="product.price"
                :size="product.size"
                :image="product.image"
            />
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
            products: [
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
                }
            ]
        }
    },
    computed: {
        productRows() {
            const rows = []
            for (let i = 0; i < this.products.length; i += 3) {
                rows.push(this.products.slice(i, i + 3))
            }
            return rows
        }
    }
}
</script>

<style scoped>
.products-grid {
    width: 100%;
    padding-top: 20px;
}

.products-row {
    display: flex;
    justify-content: flex-end;
    gap: 40px;
    margin-bottom: 15px;
}

@media (max-width: 900px) {
    .products-row {
        flex-wrap: wrap;
        gap: 10px;
    }
}
</style>