<template>
    <div class="profile_wrapper">
        <div class="image_profile"><img src="./../../assets/images/User.png" alt=""></div>
        <span class="profile_title" @click="openModal">Войти</span>

        <Login
        v-if="isModalOpen"
        :is-visible="isModalOpen"
        @close="closeModal"
        />
    </div>
</template>

<script setup lang="ts">
import Login from '@/components/modal/Login.vue'
import { ref } from 'vue'


const isModalOpen = ref<boolean>(false)

const openModal = (): void => {
  isModalOpen.value = true
}

const closeModal = (): void => {
  isModalOpen.value = false
}
</script>

<style scoped lang="scss">
    .profile_title{
        font-size: var(--text-xs);
        font-family: var(--font-family);
        color: var(--text-color);
    }
    .image_profile{
        margin: 1px 7px 0px 0px;
    }
    .profile_wrapper{
        display: flex;
        flex-wrap: nowrap;
    }
</style>