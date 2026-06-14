<script setup lang="ts">
import Button from '@/components/ui/Button.vue'

defineProps<{
    bgColor?: string
    image?: string
    title?: string
    description?: string
    date?: string
    icon?: string
}>()
</script>

<template>
    <div class="news-card">
        <div class="card-image" :style="{ backgroundImage: `url(${image})` }">
            <Button 
                theme="icon" 
                :icon="icon" 
                class="round-btn"
            />
            <div class="image-gradient"></div>
        </div>
        
        <div class="card-content">
            <h3 class="card-title">{{ title }}</h3>
            <p class="card-description">{{ description }}</p>
            <span class="card-date">{{ date }}</span>
        </div>
    </div>
</template>

<style scoped lang="scss">
.news-card {
    border-radius: 12px;
    overflow: hidden;
    width: 360px;
    background-color: var(--color-dark-blue);
    display: flex;
    flex-direction: column;
}
.card-image {
    position: relative;
    width: 100%;
    height: 200px;
    background-size: cover;
    background-position: center;
    flex-shrink: 0;
}

.round-btn {
    position: absolute;
    top: 12px;
    right: 12px;
    z-index: 10;
}

.image-gradient {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 100px;
    background: linear-gradient(
        to bottom,
        transparent 0%,
        var(--color-dark-blue) 100%
    );
    pointer-events: none;
}

.card-content {
    padding: 20px 20px 30px 20px;
    display: flex;
    flex-direction: column;
    background-color: var(--color-dark-blue);
    margin-top: -20px;
}

.card-title {
    font-size: var(--text-lg);
    font-family: var(--font-family);
    color: var(--text-color);
    margin: 0;
}

.card-description {
    font-size: var(--text-sm);
    font-family: var(--font-family);
    color: var(--text-color);
    line-height: 1.4;
    margin-top: 12px;
}

.card-date {
    font-size: var(--text-xs);
    font-family: var(--font-family);
    color: var(--text-color);
    margin-top: 12px;
}
</style>