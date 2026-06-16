<script setup lang="ts">
import Title from '@/components/ui/Title.vue'
import Card_icon from '@/components/aboutp/Card_icon.vue';
</script>

<template>
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
            </div>
            <div class="cont_icon_second">
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
</template>

<style scoped lang="scss">
    .wrapper_cont_icon{
        max-width: 100%;
        max-height: 1066px;
        background-color: var(--saka-color);
    }
    .title_com{
        padding: 50px 0px 0px 220px;
        width: 700px;
    }
    .wrapper_cont_icon_second{
        background-image: url(./../../assets/images/lenta.png);
        background-repeat: no-repeat;
        background-position: right center;
        max-width: 100%;
        max-height: 821px;
        margin-left: 200px;
    }
    .cont_icon{
        background-position: right center;
        max-width: 100%;
        max-height: 245px;
    }
    .cont_icon_first{
        gap: 30px;
        display: flex;
        flex-wrap: nowrap;
    }
    .cont_icon_second{
        gap: 30px;
        display: flex;
        flex-wrap: nowrap;
        margin-top: 30px;
    }
</style>