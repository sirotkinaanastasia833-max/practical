<template>
    <Container>
        <div class="gallery_wrapper">
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
        </div>
    </Container>
</template>

<script setup lang="ts">
import T_shirt from '@/components/homep/T_shirt.vue'
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
.gallery {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
    gap: 70px;
    @include tablet {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        padding-left: 30px;
    }
    @include mobile {
        display: grid;
        grid-template-columns: 1fr 1fr;
        padding-left: 40px;
    }
}
.gallery_wrapper{
    display: flex;
    justify-content: center;
    @include tablet {
        display: flex;
        justify-content: flex-start;
    }
    @include mobile {
        display: flex;
        justify-content: flex-start;
    }
}
</style>