<template>
    <Container>
        <div class="wrapper_text_nav">
            <span class="glavnaya">ГЛАВНАЯ</span>
            <span class="arrow">></span>
            <span class="catalog">КАТАЛОГ</span>
        </div>
    </Container>
</template>

<script setup lang="ts">
import Container from '../layout/Container.vue';

</script>

<style scoped lang="scss">
    .wrapper_text_nav{
        display: flex;
        justify-content: flex-start;
        padding-top: 30px;
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