<script setup lang="ts">
import Saka_tekstil_header from '@/components/aboutp/Saka_tekstil_header.vue';
import Saka_tekstil_tur from '@/components/aboutp/Saka_tekstil_tur.vue';
import Container_saka_tekstil from '@/components/aboutp/Container_saka_tekstil.vue';
import Container_icon_saka from '@/components/aboutp/Container_icon_saka.vue';
import Sertifikat from '../components/ui/Sertifikat.vue';
import Group_title from '@/components/aboutp/Group_title.vue';
import Product_carousel from '../components/ui/Product_carousel.vue';

</script>

<template>
    <div class="block_theme">
        <Saka_tekstil_header />
        <Saka_tekstil_tur/>
        <Container_saka_tekstil />
        <Container_icon_saka/>
        <Sertifikat/>
        <Group_title/>
        <Product_carousel/>
    </div>
</template>

<style scoped lang="scss">
    .block_theme{
        background-color: var(--background);
    }
</style>