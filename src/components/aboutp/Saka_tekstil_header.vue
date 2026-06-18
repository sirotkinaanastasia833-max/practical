<script setup lang="ts">
import Text_nav from '@/components/catalogp/Text_nav.vue';
import Title from '@/components/ui/Title.vue'
import Container from '../layout/Container.vue';
</script>

<template>
    <Container>
        <div class="nav_text_wrapper">
            <Text_nav/>
            <Title theme="left" text="О компании" class="title_com" />
        </div>
    </Container>
</template>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
    .title_com{
        width: 700px;
        display: flex;
        justify-content: start;
        padding: 30px 0px;
        color: var(--text-color-black);
        @include mobile{
            width: 300px;
            font-size: var(--text-2xl);
        }
    }
    .nav_text_wrapper{
        padding-left: 20px;
    }
</style>