<script setup lang="ts">
import Container_text from '@/components/catalogp/Container_text.vue'
import Product_carousel from '@/components/ui/Product_carousel.vue'
import Big_container from '@/components/catalogp/Big_container.vue';
</script>

<template>
    <div class="block_theme">
        <Container_text />
        <Big_container />
        <Product_carousel/>
    </div>
</template>

<style scoped lang="scss">
    .block_theme{
        background-color: var(--background);
    }
</style>