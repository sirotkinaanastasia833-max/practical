<template>
    <Container>
        <h3>Saka Tekstil дорожит своей репутацией</h3>
        <div class="sertifikat">
            <div class="arrow left" @click="prevSlide">
                <img src="./../../assets/images/ArrowRight.png" alt="назад">
            </div>
            
            <div class="sertifikat-wrapper">
                <div class="sertifikat-track" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
                    <div class="sertifikat-page" v-for="(page, index) in pages" :key="index">
                        <img 
                            v-for="(sert, idx) in page" 
                            :key="idx"
                            :src="sert" 
                            alt="сертификат" 
                            class="sert"
                        />
                    </div>
                </div>
            </div>
            <div class="arrow right" @click="nextSlide">
                <img src="./../../assets/images/ArrowRight.png" alt="вперед">
            </div>
        </div>
    </Container>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'
import Container from '../layout/Container.vue'

const currentIndex = ref<number>(0)

const sertifikats = [
    '/src/assets/images/sert1.png',
    '/src/assets/images/sert2.png',
    '/src/assets/images/sert3.png',
    '/src/assets/images/sert1.png',
    '/src/assets/images/sert2.png',
    '/src/assets/images/sert3.png'
]

const pages = computed(() => {
    const result: string[][] = []
    for (let i = 0; i < sertifikats.length; i += 3) {
        result.push(sertifikats.slice(i, i + 3))
    }
    return result
})

const totalPages = computed(() => pages.value.length)

const nextSlide = (): void => {
    currentIndex.value = (currentIndex.value + 1) % totalPages.value
}

const prevSlide = (): void => {
    currentIndex.value = (currentIndex.value - 1 + totalPages.value) % totalPages.value
}
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;

h3 {
    font-size: var(--text-2xl);
    font-family: var(--font-family);
    text-align: center;
    margin-bottom: 40px;
    color: var(--text-color-black);
    padding-top: 30px;
    @include tablet {
        font-size: 26px;
    }

    @include mobile {
        font-size: 20px;
    }
}

.sertifikat {
    display: flex;
    align-items: center;
    gap: 20px;
    padding: 0 60px;

    @include tablet {
        padding: 0 40px;
        gap: 16px;
    }

    @include mobile {
        padding: 0 16px;
        gap: 10px;
        justify-content: center;
    }
}

.arrow {
    background-color: var(--saka-color);
    border-radius: 50%;
    width: 50px;
    height: 50px;
    cursor: pointer;
    transition: all 0.3s ease;
    flex-shrink: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 10;

    &:hover {
        background-color: var(--dark-gold);
        transform: scale(1.1);
    }

    img {
        width: 20px;
        height: 20px;
        margin: 0;
    }

    &.left img {
        transform: rotate(180deg);
    }

    @include tablet {
        width: 40px;
        height: 40px;

        img {
            width: 16px;
            height: 16px;
        }
    }

    @include mobile {
        width: 30px;
        height: 30px;

        img {
            width: 12px;
            height: 12px;
        }
    }
}

.sertifikat-wrapper {
    overflow: hidden;
    flex: 1;

    @include mobile {
        display: flex;
        justify-content: center;
    }
}

.sertifikat-track {
    display: flex;
    transition: transform 0.5s ease;
}

.sertifikat-page {
    display: flex;
    flex-shrink: 0;
    width: 100%;
    justify-content: center;
    gap: 40px;

    @include tablet {
        gap: 0;
        justify-content: center;
    }

    @include mobile {
        gap: 0;
        justify-content: center;
    }
}

.sert {
    width: 260px;
    height:


350px;
    object-fit: cover;
    border-radius: 12px;

    @include tablet {
        width: 360px;
        height: 504px;
    }

    @include mobile {
        width: 195px;
        height: 280px;
        margin: 0 auto;
    }
}

@include tablet {
    .sertifikat-page .sert:nth-child(2),
    .sertifikat-page .sert:nth-child(3) {
        display: none;
    }
}

@include mobile {
    .sertifikat-page .sert:nth-child(2),
    .sertifikat-page .sert:nth-child(3) {
        display: none;
    }

    .sertifikat-wrapper {
        display: flex;
        justify-content: center;
    }

    .sertifikat-page {
        justify-content: center;
    }
}
</style>


