<script setup lang="ts">
import Stocks from '@/components/homep/Stocks.vue';
import Carousel from '@/components/homep/Carousel.vue'
import Card_container from '@/components/homep/Card_container.vue'
import Fabric_container from '@/components/homep/Fabric_container.vue'
import Saka_tekstil from '@/components/homep/Saka_tekstil.vue'
import Sertifikat from '@/components/ui/Sertifikat.vue'
import Container_preface from '@/components/homep/Container_preface.vue';
import Container_t_shirt from '@/components/homep/Container_t_shirt.vue';
import Forma from '@/components/homep/Forma.vue'
import Product_carousel from '@/components/ui/Product_carousel.vue'
import Title_pallette from '@/components/homep/Title_pallette.vue';
</script>

<template>
    <div class="block_theme">
        <Stocks class="Stocks" />
        <Carousel/>
        <Card_container/>
        <Fabric_container />
        <Saka_tekstil/>
        <Sertifikat/>
        <Container_preface />
        <Container_t_shirt />
        <Title_pallette />
        <Container_t_shirt />
        <Forma/>
        <Product_carousel/>
    </div>
</template>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
    .Stocks{
        @include tablet {
            display: none;
        }
    }
    .block_theme{
        background-color: var(--background);
    }
</style>