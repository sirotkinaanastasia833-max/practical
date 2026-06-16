<script setup lang="ts">
import Title from '@/components/ui/Title.vue'
import Saka_tekstil_card from '@/components/aboutp/Saka_tekstil_card.vue'
</script>

<template>
    <Title theme="left" text="Saka Tekstil работает с трикотажными полотнами разного качества:" class="title_com" />
    <div class="container_Saka_tekstil_card">
        <Saka_tekstil_card
            image="/src/assets/images/shelk_tekstil.png"
            title="Open end"
            description="Бюджетный трикотаж, имеет ворсистую и шероховатую поверхность из-за коротких волокон."
            :width="358"
            :image-height="170"
        />
        <Saka_tekstil_card
            image="/src/assets/images/green_tekstil.png"
            title="Пенье компакт"
            description="Высшее качество трикотажной ткани, имееют гладкую поверхность без ворсинок"
            :width="358"
            :image-height="170"
        />
        <Saka_tekstil_card
            image="/src/assets/images/haki_tekstil.png"
            title="Пенье компакт Плюс-EXCLUSIVE"
            description="полотно вяжется американскими нитками  и окрашено немецкими красками высшего качества"
            :width="358"
            :image-height="170"
        />
    </div>
</template>

<style scoped lang="scss">
    .title_com{
        padding: 15px 0px 0px 220px;
        width: 700px;
    }
    .container_Saka_tekstil_card{
        display: flex;
        flex-wrap: nowrap;
        gap: 50px;
        justify-content: center;
        margin: 30px 0px 0px 40px;
    }
</style>