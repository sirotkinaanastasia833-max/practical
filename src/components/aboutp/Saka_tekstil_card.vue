<script setup lang="ts">
defineProps<{
    image?: string
    title?: string
    description?: string
    width?: number
    imageHeight?: number
}>()
</script>

<template>
    <div class="image-card" :style="{ width: width ? width + 'px' : 'auto' }">
        <div class="card-image" :style="{ height: imageHeight ? imageHeight + 'px' : '200px' }">
            <img :src="image" :alt="title">
        </div>
        <p class="card-title">{{ title }}</p>
        <p class="card-description">{{ description }}</p>
    </div>
</template>

<style scoped lang="scss">
.image-card {
    display: flex;
    flex-direction: column;
    .card-image {
        width: 100%;
        overflow: hidden;
        border-radius: 16px;
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    .card-title {
        margin-top: 12px;
        font-size: var(--text-sm);
        color: var(--text-color-black);
        text-align: left;
        font-weight: bolder;
        font-family: var(--font-family);
    }
    .card-description{
        margin-top: -10px;
        font-size: var(--text-sm);
        color: var(--text-color-black);
        text-align: left;
        font-weight: 200;
        font-family: var(--font-family);
    }
}
</style>