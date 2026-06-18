<script setup lang="ts">
import Title from '@/components/ui/Title.vue';
import Container from '../layout/Container.vue';
</script>
<template>
    <Container><Title thema="left" text="Сезонная палитра" class="preface_title"/></Container>
</template>
<style scoped lang="scss">
    .preface_title{
        max-width: 100%;
        display: flex;
        justify-content: flex-start;
        color: var(--text-color-black);
    }
</style>