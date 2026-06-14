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
    height: 400px;
    background-color: var(--color-dark-blue);
    
    .card-image {
        position: relative;
        width: 360px;
        height: 200px;
        background-size: cover;
        background-position: center;
        
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
            height: 120px;
            background: linear-gradient(
                to bottom,
                transparent 0%,
                var(--color-dark-blue) 100%
            );
            pointer-events: none;
        }
    }
    
    .card-content {
        padding: 40px;
        display: flex;
        flex-direction: column;
        margin-top: -90px;
        position: relative;
        z-index: 2;
    }
    
    .card-title {
        font-size: var(--text-lg);
        font-family: var(--font-family);
        color: var(--text-color);
    }
    
    .card-description {
        font-size: var(--text-sm);
        font-family: var(--font-family);
        color: var(--text-color);
        line-height: 1.4;
        margin-top: 15px;
    }
    
    .card-date {
        font-size: var(--text-xs);
        font-family: var(--font-family);
        color: var(--text-color);
        margin-top: 17px;
    }
}
</style>