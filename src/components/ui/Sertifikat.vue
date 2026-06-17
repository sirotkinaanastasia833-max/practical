<template>
    <div>
        <h3>Saka Tekstil дорожит своей репутацией</h3>
        <div class="sertifikat">
            <div class="arrow" @click="prevSlide">
                <img src="./../../assets/images/ArrowLeft.png" alt="">
            </div>
            
            <div class="sertifikat-wrapper">
                <div class="sertifikat-track" :style="{ transform: 'translateX(-' + currentIndex * 100 + '%)' }">
                    <div class="sertifikat-page">
                        <img src="./../../assets/images/sert1.png" alt="" class="sert">
                        <img src="./../../assets/images/sert2.png" alt="" class="sert">
                        <img src="./../../assets/images/sert3.png" alt="" class="sert">
                    </div>
                    <div class="sertifikat-page">
                        <img src="./../../assets/images/sert1.png" alt="" class="sert">
                        <img src="./../../assets/images/sert2.png" alt="" class="sert">
                        <img src="./../../assets/images/sert3.png" alt="" class="sert">
                    </div>
                </div>
            </div>
            
            <div class="arrow" @click="nextSlide">
                <img src="./../../assets/images/ArrowRight.png" alt="">
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const currentIndex = ref<number>(0)

const nextSlide = (): void => {
    currentIndex.value = currentIndex.value === 0 ? 1 : 0
}

const prevSlide = (): void => {
    currentIndex.value = currentIndex.value === 0 ? 1 : 0
}
</script>

<style scoped lang="scss">
h3 {
    font-size: var(--text-2xl);
    font-family: var(--font-family);
    margin: 60px 0px 30px 470px;
}

.arrow {
    background-color: var(--saka-color);
    border-radius: 50%;
    width: 50px;
    height: 50px;
    cursor: pointer;
    transition: all 0.3s ease;
    flex-shrink: 0;
    margin-top: 220px;

    &:hover {
        background-color: var(--dark-gold);
        transform: scale(1.1);
    }

    img {
        margin: 12px 0px 0px 12px;
    }
}

.sertifikat {
    display: flex;
    flex-wrap: nowrap;
    margin-left: 60px;
    margin-right: 60px;
    align-items: flex-start;
    gap: 20px;
}

.sertifikat-wrapper {
    overflow: hidden;
    flex: 1;
}

.sertifikat-track {
    display: flex;
    transition: transform 0.4s ease;
}

.sertifikat-page {
    display: flex;
    flex-shrink: 0;
    width: 100%;
    justify-content: center;
    gap: 40px;
}

.sert {
    margin-right: 0;
}
</style>