<script setup lang="ts">
defineProps<{
    image?: string
    title?: string
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
    </div>
</template>

<style scoped lang="scss">
.image-card {
    display: flex;
    flex-direction: column;
    
    .card-image {
        width: 100%;
        overflow: hidden;
        border-radius: 8px;
        
        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    
    .card-title {
        margin-top: 12px;
        font-size: var(--text-base);
        font-weight: 500;
        color: var(--text-color-black);
        text-align: center;
    }
}
</style>