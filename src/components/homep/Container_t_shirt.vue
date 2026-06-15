<template>
    <div class="gallery">
        <T_shirt
            image="/src/assets/images/dark_grey_t-shirt.png"
            title="A-104 Dark Grey"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/grey_t-shirt.png"
            title="A-101 Grey"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/white_t-shirt.png"
            title="A-115 White"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/black_t-shirt.png"
            title="A-123 Black"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/dark_blue_t-shirt.png"
            title="A-106 Dark Blue"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/blue_t-shirt.png"
            title="A-107 Blue"
            :width="100"
            :image-height="80"
        />
    </div>
    <div class="gallery_second">
        <T_shirt
            image="/src/assets/images/light_blue_t-shirt.png"
            title="A-118 Light Blue"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/orange_t-shirt.png"
            title="A-135 Orange"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/green_t-shirt.png"
            title="A-136 Green"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/yellow_t-shirt.png"
            title="A-125 Yellow"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/purple_t-shirt.png"
            title="A-201 Purple"
            :width="100"
            :image-height="80"
        />
        <T_shirt
            image="/src/assets/images/red_t-shirt.png"
            title="A-100 Red"
            :width="100"
            :image-height="80"
        />
    </div>
</template>

<script setup lang="ts">
import T_shirt from '@/components/homep/T_shirt.vue'
</script>

<style scoped>
.gallery {
    display: flex;
    gap: 100px;
    flex-wrap: wrap;
    justify-content: center;
}
.gallery_second{
    display: flex;
    gap: 100px;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 80px;   
}
</style>