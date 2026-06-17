<template>
    <Container>
        <div class="container_text_wrapper">
            <Text_nav/>
            <Title theme="left" text="Позаботьтесь о себе и своих близких, выбирайте качественные ткани" class="title_com" />
            <Filter />
        </div>
    </Container>
</template>
<script setup lang="ts">
import Text_nav from '@/components/catalogp/Text_nav.vue';
import Title from '@/components/ui/Title.vue'
import Filter from '@/components/catalogp/Filter.vue';
import Container from '../layout/Container.vue';
</script>
<style scoped lang="scss">
    .title_com{
        width: 700px;
        display: flex;
        justify-content: flex-start;
        padding-top: 30px;
    }
    .container_text_wrapper{
        margin-left: 50px;
    }
</style>