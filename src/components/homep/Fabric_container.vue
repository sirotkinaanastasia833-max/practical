<template>
    <Container>
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
    </Container>
</template>

<script setup lang="ts">
import Title from '@/components/ui/Title.vue'
import Fabric from '@/components/homep/Fabric.vue'
import Button from '@/components/ui/Button.vue'
import { ref, onMounted, onUnmounted } from 'vue'
import Container from '../layout/Container.vue'

const imageSizes = [
    { 
        image: '/src/assets/images/blue_fabric.png', 
        text: 'Футер 3-х Нитка',
        desktop: { width: 460, height: 210 },
        tablet: { width: 380, height: 210 },
        mobile: { width: 150, height: 120 }
    },
    { 
        image: '/src/assets/images/grey_fabric.png', 
        text: 'Френч Терри',
        desktop: { width: 260, height: 210 },
        tablet: { width: 220, height: 210 },
        mobile: { width: 300, height: 210 }
    },
    { 
        image: '/src/assets/images/pink_fabric.png', 
        text: 'Вискоза',
        desktop: { width: 360, height: 210 },
        tablet: { width: 300, height: 210 },
        mobile: { width: 300, height: 210 }
    },
    { 
        image: '/src/assets/images/dark_blue.png', 
        text: 'Пике',
        desktop: { width: 260, height: 210 },
        tablet: { width: 300, height: 210 },
        mobile: { width: 300, height: 210 }
    },
    { 
        image: '/src/assets/images/dark_grey.png', 
        text: 'Кулинарная гладь',
        desktop: { width: 360, height: 210 },
        tablet: { width: 380, height: 210 },
        mobile: { width: 300, height: 210 }
    },
    { 
        image: '/src/assets/images/purple_fabric.png', 
        text: 'Бифлекс',
        desktop: { width: 460, height: 210 },
        tablet: { width: 220, height: 210 },
        mobile: { width: 300, height: 210 }
    }
]

const windowWidth = ref(window.innerWidth)

const getDeviceType = () => {
    const width = windowWidth.value
    if (width >= 1024) return 'desktop'
    if (width >= 640) return 'tablet'
    return 'mobile'
}

const getSize = (sizes: any) => {
    const device = getDeviceType()
    return sizes[device]
}

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

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;

.fabric_container {
    max-width: 100%;
    background-color: var(--color-dark-blue);
    padding-bottom: 60px;
    display: flex;
    flex-direction: column;
    margin: 30px 0px;

}

.title_fabric {
    color: var(--text-color);
    font-family: var(--font-family);
    font-size: var(--text-2xl);
    max-width: 500px;
    word-break: break-word;
    padding-top: 30px;
    width: 100%;
    padding-left: 200px;  

    @include tablet {
        padding-left: 50px;
        font-size: 24px;
        max-width: 350px;
    }

    @include mobile {
        padding-left: 20px;
        font-size: 20px;
        max-width: 250px;
    }
}

.wrapper_fabric {
    display: flex;
    flex-wrap: wrap;
    justify-content: center; 
    gap: 30px;
    max-width: 1400px;      
    padding: 0 20px;
    margin: 0 auto;  

    @include tablet {
        gap: 16px;
        padding: 0 16px;
    }

    @include mobile {
        gap: 12px;
        padding: 0 12px;
    }
}

.image-wrapper {
    position: relative;
    display: inline-block;
    flex: 0 0 auto;
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