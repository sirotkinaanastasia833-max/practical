<script setup lang="ts">
import Uiicon from '@/components/ui/Uiicon.vue'

defineProps<{
    icon?: string
    title?: string
    description?: string
    width?: number
    iconHeight?: number
}>()


</script>

<template>
    <div class="card_icon">
        <Uiicon :name="icon" class="icon"/>
        <h1 class="card_icon_title">{{ title }}</h1>
        <p class="card_icon_description">{{description}}</p>
    </div>
</template>

<style scoped lang="scss">
    .card_icon{
        background-color: var(--text-color);
        width: 220px;
        height: 337px;
        color: var(--text-color-black);
        padding: 0px 20px 0px 20px;
        border-radius: 16px;
        font-family: var(--font-family);
        text-align: center;
    }
    .card_icon_title{
        font-size: var(--text-sm);
        margin-top: 20px;
    }
    .card_icon_description{
        font-size: var(--text-sm);
        margin-top: 20px;
    }
    .icon{
        margin-top: 60px;
    }
</style>