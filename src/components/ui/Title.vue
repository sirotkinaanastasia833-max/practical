<script setup lang="ts">
defineProps<{
    theme?: 'left' | 'center' | 'right'
    text?: string
}>()
</script>

<template>
    <p class="title" :class="'title--${theme}'">
        {{ text }}
    </p>
</template>

<style lang="scss">
    .title{
        font-size: 26px;
        letter-spacing: 2%;
        font-weight: 600;
        font-family: var(--font-family);

        &--center{
            text-align: center;
        }

        &--left{
            text-align: left;
        }

        &--right{
            text-align: right;
        }
    }
</style>