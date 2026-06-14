<template>
    <div class="news-list">
        <div class="card_wrapper">
            <Card
                bgColor="'var(----color-dark-blue)'"
                image="/src/assets/images/Saka_home.png"
                title="Пример текста для заголовка новости"
                description="Здесь будет находиться небольшое триггерное описание или краткий дискриптор новости"
                date="31.03.2022"
                icon="/src/assets/images/arrow_ring.png"
            />
            <Card
                bgColor="'var(----color-dark-blue)'"
                image="/src/assets/images/homes_saka.png"
                title="Пример текста для заголовка новости"
                description="Здесь будет находиться небольшое триггерное описание или краткий дискриптор новости"
                date="31.03.2022"
                icon="/src/assets/images/arrow_ring.png"
            />
            <Card
                bgColor="'var(----color-dark-blue)'"
                image="/src/assets/images/factory.png"
                title="Пример текста для заголовка новости"
                description="Здесь будет находиться небольшое триггерное описание или краткий дискриптор новости"
                date="31.03.2022"
                icon="/src/assets/images/arrow_ring.png"
            />
        </div>
        <div class="card_wrapper">
            <Card
                bgColor="'var(----color-dark-blue)'"
                image="/src/assets/images/home_flags.png"
                title="Пример текста для заголовка новости"
                description="Здесь будет находиться небольшое триггерное описание или краткий дискриптор новости"
                date="31.03.2022"
                icon="/src/assets/images/arrow_ring.png"
            />
            <Card
                bgColor="'var(----color-dark-blue)'"
                image="/src/assets/images/flags.png"
                title="Пример текста для заголовка новости"
                description="Здесь будет находиться небольшое триггерное описание или краткий дискриптор новости"
                date="31.03.2022"
                icon="/src/assets/images/arrow_ring.png"
            />
            <Card
                bgColor="'var(----color-dark-blue)'"
                image="/src/assets/images/big_home.png"
                title="Пример текста для заголовка новости"
                description="Здесь будет находиться небольшое триггерное описание или краткий дискриптор новости"
                date="31.03.2022"
                icon="/src/assets/images/arrow_ring.png"
            />
        </div>
    </div>
</template>

<script setup lang="ts">
import Card from '@/components/homep/Card.vue'
</script>

<style scoped>
.card_wrapper{
    display: flex;
    flex-wrap: nowrap;
    justify-content: center;
    gap: 20px;
}
.news-list {
    display: flex;
    flex-direction: column;
    gap: 20px;
    max-width: 100%;
    margin-left: 54px;
    margin-top: 20px;
}
</style>