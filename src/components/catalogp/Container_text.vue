<template>
    <Text_nav/>
    <Title theme="left" text="Позаботьтесь о себе и своих близких, выбирайте качественные ткани" class="title_com" />
    <Filter />
</template>
<script setup lang="ts">
import Text_nav from '@/components/catalogp/Text_nav.vue';
import Title from '@/components/ui/Title.vue'
import Filter from '@/components/catalogp/Filter.vue';
</script>
<style scoped lang="scss">
    .title_com{
        padding: 15px 0px 0px 220px;
        width: 700px;
    }
</style>