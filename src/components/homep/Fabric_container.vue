<script setup lang="ts">
import Title from '@/components/ui/Title.vue'
import Fabric from '@/components/homep/Fabric.vue'
import Button from '@/components/ui/Button.vue'
import { ref, onMounted, onUnmounted } from 'vue'

// Данные о картинках с размерами для разных экранов
const imageSizes = [
    { 
        image: '/src/assets/images/blue_fabric.png', 
        text: 'Футер 3-х Нитка',
        desktop: { width: 460, height: 210 },
        tablet: { width: 200, height: 160 },
        mobile: { width: 150, height: 120 }
    },
    { 
        image: '/src/assets/images/grey_fabric.png', 
        text: 'Френч Терри',
        desktop: { width: 260, height: 210 },
        tablet: { width: 200, height: 160 },
        mobile: { width: 150, height: 120 }
    },
    { 
        image: '/src/assets/images/pink_fabric.png', 
        text: 'Вискоза',
        desktop: { width: 360, height: 210 },
        tablet: { width: 200, height: 160 },
        mobile: { width: 150, height: 120 }
    },
    { 
        image: '/src/assets/images/dark_blue.png', 
        text: 'Пике',
        desktop: { width: 260, height: 210 },
        tablet: { width: 200, height: 160 },
        mobile: { width: 150, height: 120 }
    },
    { 
        image: '/src/assets/images/dark_grey.png', 
        text: 'Кулинарная гладь',
        desktop: { width: 360, height: 210 },
        tablet: { width: 200, height: 160 },
        mobile: { width: 150, height: 120 }
    },
    { 
        image: '/src/assets/images/purple_fabric.png', 
        text: 'Бифлекс',
        desktop: { width: 460, height: 210 },
        tablet: { width: 200, height: 160 },
        mobile: { width: 150, height: 120 }
    }
]

// Текущая ширина экрана
const windowWidth = ref(window.innerWidth)

// Определяем тип устройства
const getDeviceType = () => {
    const width = windowWidth.value
    if (width >= 1024) return 'desktop'
    if (width >= 640) return 'tablet'
    return 'mobile'
}

// Получаем размеры для текущего устройства
const getSize = (sizes: any) => {
    const device = getDeviceType()
    return sizes[device]
}

// Обновляем ширину при ресайзе
const updateWidth = () => {
    windowWidth.value = window.innerWidth
}

onMounted(() => {
    window.addEventListener('resize', updateWidth)
})

onUnmounted(() => {
    window.removeEventListener('resize', updateWidth)
})
</script>

<template>
    <div class="fabric_container">
        <Title theme="left" text="Выбирайте из множества разновидностей тканей" class="title_fabric"/>
        
        <div class="wrapper_fabric">
            <div class="image-wrapper" v-for="(item, index) in imageSizes" :key="index">
                <Fabric 
                    :image="item.image" 
                    :width="getSize(item).width" 
                    :height="getSize(item).height" 
                    class="Fabric_image" 
                />
                <Button theme="text" :text="item.text" class="fabric-btn" />
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;

.fabric_container {
    max-width: 100%;
    max-height: 760px;
    background-color: var(--color-dark-blue);
    padding-bottom: 90px;
}

.title_fabric {
    color: var(--text-color);
    font-family: var(--font-family);
    font-size: var(--text-2xl);
    max-width: 500px;
    word-break: break-word;
    margin-left: 200px;
    padding-top: 90px;

    @include tablet {
        margin-left: 50px;
        font-size: 24px;
        max-width: 350px;
    }

    @include mobile {
        margin-left: 20px;
        font-size: 20px;
        max-width: 250px;
    }
}

.wrapper_fabric {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 30px;
    margin-left: 200px;

    @include tablet {
        grid-template-columns: repeat(2, 1fr);
        margin-left: 50px;
        gap: 16px;
    }

    @include mobile {
        grid-template-columns: repeat(2, 1fr);
        margin-left: 16px;
        gap: 12px;
    }
}

.image-wrapper {
    position: relative;
    display: inline-block;
}

.fabric-btn {
    position: absolute;
    bottom: 25px;
    left: 25px;

    @include tablet {
        bottom: 15px;
        left: 15px;
    }

    @include mobile {
        bottom: 10px;
        left: 10px;
    }
}

.Fabric_image {
    object-fit: cover;
}
</style>