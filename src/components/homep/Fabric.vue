<script setup lang="ts">
defineProps<{
    image?: string
    width?: number
    height?: number
}>()
</script>

<template>
    <div class="fabric-image" :style="{ width: width ? width + 'px' : 'auto', height: height ? height + 'px' : 'auto' }">
        <img :src="image" alt="">
    </div>
</template>

<style scoped lang="scss">
.fabric-image {
    overflow: hidden;
    
    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
}
</style>