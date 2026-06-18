<script setup lang="ts">
import { ref } from 'vue'
import Container from '../layout/Container.vue';
const price = ref(50000)
</script>

<template>
   <Container>
        <div class="Container_wrapper_filter">
             <div class="slider">
                <div class="min">0₽</div>
                <input type="range" v-model="price" min="0" max="100000">
                <div>{{ price }}₽</div>
            </div>
        </div>
   </Container>
</template>

<style scoped lang="scss">
.Container_wrapper_filter{
    display: flex;
    justify-content: center;
}
.slider {
    display: flex;
    align-items: center;
    gap: 10px;
    color: var(--text-color-black);
    background-color: var(--saka-color);
    width: 330px;
    height: 90px;
    padding: 20px;
    border-radius: 16px;
    margin-top: 10px;
}

input {
    width: 223px;
    height: 3px;
    -webkit-appearance: none;
    background: rgba(0, 0, 0, 0.2);
    border-radius: 3px;
}
input::-webkit-slider-thumb {
    -webkit-appearance: none;
    width: 14px;
    height: 14px;
    border-radius: 50%;
    background: var(--dark-gold);
    cursor: pointer;
}

</style>