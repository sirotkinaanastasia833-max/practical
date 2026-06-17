<template>
    <div class="card">
        <div class="card-image">
            <img :src="image" alt="">
        </div>
        <div class="card-content">
            <p class="card-title">{{ title }}</p>
            <div class="info">
                <p class="card-price">{{ price }}$</p>
                <p class="card-size">{{ size }} см</p>
            </div>
            <Button theme="full" text="Подробнее" icon="/src/assets/images/arrow.png" class="product-button"/>
        </div>
    </div>
</template>

<script setup lang="ts">
import Button from '@/components/ui/Button.vue'

interface Props {
    title?: string
    price?: string | number
    size?: string | number
    image?: string
}

withDefaults(defineProps<Props>(), {
    title: 'Кулинарная гладь',
    price: '11,4',
    size: '180',
    image: '/src/assets/images/blue.png'
})
</script>

<style scoped lang="scss">
.card {
    width: 260px;
    height: 430px;
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);

    &-image {
        width: 100%;
        height: 260px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }

    &-content {
        padding: 15px;
    }

    &-title {
        font-size: var(--text-lg);
        font-weight: 600;
        margin-bottom: 8px;
        font-family: var(--font-family);
    }

    &-price {
        font-size: var(--text-xl);
        font-weight: 600;
        font-family: var(--font-family);
    }

    &-size {
        font-size: var(--text-sm);
        color: var(--size-color);
        margin-top: 25px;
        font-family: var(--font-family);
    }
}

.info {
    display: flex;
    flex-wrap: nowrap;
    gap: 15px;
    margin-top: -20px;
}

.product-button {
    width: 220px;
    height: 55px;
    margin-left: 1px;
    justify-content: space-between;
    padding-left: 20px;
    padding-right: 30px;
}
</style>