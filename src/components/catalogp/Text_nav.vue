<template>
    <div class="wrapper_text_nav">
        <span class="glavnaya">ГЛАВНАЯ</span>
        <span class="arrow">></span>
        <span class="catalog">КАТАЛОГ</span>
    </div>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
    .wrapper_text_nav{
        padding: 60px 0px 0px 220px;
    }
    .glavnaya{
        color: var(--size-color);
    }
    .arrow{
        color: var(--size-color);
        padding-left: 20px;
    }
    .catalog{
        color: var(--text-color-black);
        padding-left: 20px;
    }
</style>