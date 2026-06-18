<script setup lang="ts">
import Title from '@/components/ui/Title.vue'
import Saka_tekstil_card from '@/components/aboutp/Saka_tekstil_card.vue'
</script>

<template>
    <Container>
        <div class="wrapper_cont_saka">
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
        </div>
    </Container>
</template>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
    .title_com{
        width: 700px;
        display: flex;
        justify-content: flex-start;
        @include tablet{
            padding-left: 70px;
        }
        @include mobile{
            width: 300px;
        }
    }
    .container_Saka_tekstil_card{
        display: flex;
        flex-wrap: nowrap;
        gap: 50px;
        justify-content: center;
        margin: 30px 0px 0px 40px;
        @include tablet{
            display: grid;
            grid-template-columns: repeat(2, auto);
        }
        @include mobile{
            display: grid;
            grid-template-columns: repeat(1, auto);
            margin: 0px;
        }
    }
</style>