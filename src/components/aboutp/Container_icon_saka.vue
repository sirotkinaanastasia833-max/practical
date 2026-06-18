<script setup lang="ts">
import Title from '@/components/ui/Title.vue'
import Card_icon from '@/components/aboutp/Card_icon.vue';
import Container from '../layout/Container.vue';
</script>

<template>
    <Container>
        <div class="wrapper_cont_icon_box">
            <div class="wrapper_cont_icon">
                <div class="cont_icon"><Title theme="left" text="Наша главная задача - не просто предоставить качественную ткань, но и оказать каждому заказчику высокий уровень клиентского сервиса" class="title_com" /></div>
                <div class="wrapper_cont_icon_second">
                    <div class="cont_icon_first">
                        <Card_icon
                        icon="home"
                        title="ЛОГИСТИКА"
                        description="Весь ассортимент в наличии на складе в Москве. Вам не потребуется тратить свои ресурсы на доставку ткани из Турции."
                        :width="64"
                        :image-height="64"
                        />
                        <Card_icon
                        icon="industry"
                        title="ПРОИЗВОДСТВО"
                        description="Регулярное наличие ткани позволяет не останавливать процесс вашего производства и минимизирует финансовые потери."
                        :width="64"
                        :image-height="64"
                        />
                        <Card_icon
                        icon="dop_material"
                        title="ДОПОЛНИТЕЛЬНЫЕ МАТЕРИАЛЛЫ"
                        description="Вместе с товаром мы предоставляем полиэтиленовую упаковку, бесплатную загрузку товара со склада и бесплатные образцы."
                        :width="64"
                        :image-height="64"
                        />
                        <Card_icon
                        icon="heart"
                        title="ЛОЯЛЬНОСТЬ"
                        description="Наш трикотаж закупают известные бренды. Это позволит вам создать собственный качественный бренд одежды."
                        :width="64"
                        :image-height="64"
                        />
                        <Card_icon
                        icon="diamond"
                        title="УНИКАЛЬНОСТЬ"
                        description="Мы предоставляем клиентам широкую палитру цветов, что позволяет создавать уникальные коллекции одежды."
                        :width="64"
                        :image-height="64"
                        />
                        <Card_icon
                        icon="quality"
                        title="КАЧЕСТВО"
                        description="Наша ткань обрабатывается специальным силиконовым составом, что позволяет ей не терять свои свойства с течением времени."
                        :width="64"
                        :image-height="64"
                        />
                    </div>
                </div>
            </div>
        </div>
    </Container>
</template>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
    .wrapper_cont_icon_box{
        display: flex;
        justify-content: center;
    }
    .wrapper_cont_icon{
        max-width: 100%;
        max-height: 1066px;
        background-color: var(--saka-color);
        @include tablet{
            max-width: 698px;
            max-height: 1538px;
        }
        @include mobile{
            max-width: 360px;
            max-height: 2604px;
            background-position: right end;
        }
    }
    .title_com{
        width: 700px;
        @include tablet{
            max-width: 620px;
        }
        @include mobile{
            max-width: 300px;
            font-size: var(--text-xl);
        }
    }
    .wrapper_cont_icon_second{
        background-image: url(./../../assets/images/lenta.png);
        background-repeat: no-repeat;
        background-position: right center;
        max-width: 100%;
        max-height: 821px;
        display: flex;
        justify-content: center;
        @include tablet{
            max-width: 698px;
            max-height: 1538px;
            background-position: right end;
        }
        @include mobile{
            max-width: 360px;
            max-height: 2604px;
            background-position: right end;
        }
    }
    .cont_icon{
        background-position: right center;
        max-width: 100%;
        max-height: 245px;
    }
    .cont_icon_first{
        gap: 30px;
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        padding: 20px;
        @include tablet{
            grid-template-columns: repeat(2, auto);
        }
        @include mobile{
            grid-template-columns: repeat(1, auto);
        }
    }
</style>