<script setup lang="ts">
import Title from '@/components/ui/Title.vue';
</script>

<template>
    <div class="preface_content">
        <Title thema="left" text="Актуальная палитра “Saka Tekstil” из 45+ цветов – поможет решить любые задачи, стоящие перед вами" class="preface_title"/>
        <div class="preface_attention">
            <img src="./../../assets/images/attention.png" alt="" class="attention_img">
            <p class="attention_description">ВНИМАНИЕ! Цветопередача на вашем мониторе может значительно отличаться от оригинального цвета</p>
        </div>
    </div>
    
</template>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
    .preface_content{
        max-width: 100%;
        display: flex;
        justify-content: center;
        color: var(--text-color-black);
        @include tablet {
          flex-direction: column;
          align-items: start;
        }
    }
    .preface_title{
        padding: 80px 20px 80px 0px;
        width: 560px;
        @include tablet {
            padding: 40px 20px 0px 30px;
        }
        @include tablet {
            font-size: var(--text-xl);
            width: 300px;
        }
    }
    .preface_attention{
        width: 560px;
        height: 120px;
        border-radius: var(--border-radius-sm);
        display: flex;
        flex-wrap: nowrap;
        align-items: center;
        justify-content: center;
        border: 2px dashed var(--dark-gold);
        padding-top: 10px;
        margin: 80px 0px 0px 50px;
        @include tablet {
            margin: 0px 0px 50px 30px;
        }
        @include mobile {
            display: none;
        }
    }
    .attention_description{
        width: 370px;
        height: 72px;
        font-size: var(--text-base);
        font-family: var(--font-family);
        color: var(--text-color-black);
    }
    .attention_img{
        width: 52px;
        height: 47px;
        margin-top: -10px;
        margin-right: 20px;
    }
</style>