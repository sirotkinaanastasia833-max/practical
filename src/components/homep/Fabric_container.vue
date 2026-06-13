<script setup lang="ts">
import Title from '@/components/ui/Title.vue'
import Fabric from '@/components/homep/Fabric.vue'
import Button from '@/components/ui/Button.vue'
</script>

<template>
    <div class="fabric_container">
        <Title theme="left" text="Выбирайте из множества разновидностей тканей" class="title_fabric"/>
        
        <div class="wrapper_fabric">
            <div class="image-wrapper">
                <Fabric image="/src/assets/images/blue_fabric.png" :width="460" :height="210" />
                <Button theme="text" text="Футер 3-х Нитка" class="fabric-btn" />
            </div>
            <div class="image-wrapper">
                <Fabric image="/src/assets/images/grey_fabric.png" :width="260" :height="210" />
                <Button theme="text" text="Френч Терри" class="fabric-btn" />
            </div>
            <div class="image-wrapper">
                <Fabric image="/src/assets/images/pink_fabric.png" :width="360" :height="210" />
                <Button theme="text" text="Вискоза" class="fabric-btn" />
            </div>
        </div>
        
        <div class="wrapper_fabric_second">
            <div class="image-wrapper">
                <Fabric image="/src/assets/images/dark_blue.png" :width="260" :height="210" />
                <Button theme="text" text="Пике" class="fabric-btn" />
            </div>
            <div class="image-wrapper">
                <Fabric image="/src/assets/images/dark_grey.png" :width="360" :height="210" />
                <Button theme="text" text="Кулинарная гладь" class="fabric-btn" />
            </div>
            <div class="image-wrapper">
                <Fabric image="/src/assets/images/purple_fabric.png" :width="460" :height="210" />
                <Button theme="text" text="Бифлекс" class="fabric-btn" />
            </div>
        </div>
    </div>
</template>

<style scoped>
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
}

.wrapper_fabric {
    display: flex;
    flex-wrap: nowrap;
    gap: 30px;
    margin-left: 200px;
}

.wrapper_fabric_second {
    display: flex;
    flex-wrap: nowrap;
    gap: 30px;
    margin: 30px 0px 0px 200px;
}

.image-wrapper {
    position: relative;
    display: inline-block;
    
}

.fabric-btn {
    position: absolute;
    bottom: 25px;
    left: 25px;
    
}

</style>