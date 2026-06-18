<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps<{
    options: string[] 
    placeholder?: string
}>()

const isOpen = ref(false)
const selected = ref(props.placeholder || 'Тип полотна') 
</script>

<template>
    <div class="dropdown">
        <div class="dropdown-header" @click="isOpen = !isOpen">
            {{ selected }}
            <span class="strel">{{ isOpen ? '^' : 'v' }}</span>
        </div>
        <div class="dropdown-list" v-if="isOpen">
            <div 
                v-for="opt in options" 
                :key="opt"
                class="dropdown-item"
                @click="selected = opt; isOpen = false">
                {{ opt }}
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.strel{
    margin-left: 250px;
    margin-top: 10px;
}
.dropdown {
    position: relative;
    width: 150px;
    margin-top: -3px;
    font-family: var(--font-family);
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

.dropdown-header {
    padding: 10px;
    cursor: pointer;
    display: flex;
    justify-content: space-around;
    border-radius: 8px;
    color: var(--text-color-black);
    font-size: var(--text-xs);
}

.dropdown-list {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background: var(--saka-color);
    border-radius: 8px;
    margin-top: 5px;
    z-index: 100;
}

.dropdown-item {
    padding: 10px;
    cursor: pointer;
}

.dropdown-item:hover {
    background: var(--saka-color);
}
</style>