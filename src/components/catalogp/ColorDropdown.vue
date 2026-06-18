<script setup lang="ts">
import { ref } from 'vue'
const props = defineProps<{
    colors: string[]
    placeholder?: string
}>()
const isOpen = ref(false)
const selected = ref('')
const selectColor = (color: string) => {
    selected.value = color
    isOpen.value = false
}
</script>
<template>
    <div class="color-dropdown">
        <div class="dropdown-header" @click="isOpen = !isOpen">
            <span>{{ selected || placeholder || 'Цвет' }}</span>
            <span class="strel">{{ isOpen ? '^' : 'v' }}</span>
        </div>
        
        <div class="dropdown-list" v-if="isOpen">
            <div 
                v-for="color in colors" 
                :key="color"
                class="color-circle"
                :style="{ backgroundColor: color }"
                @click="selectColor(color)">
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.color-dropdown {
    position: relative;
    font-family: var(--font-family);
    background-color: var(--saka-color);
    width: 330px;
    height: 90px;
    padding: 20px ;
    border-radius: 16px;
    margin-top: 10px;
    font-size: var(--text-xs);
}

.dropdown-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    cursor: pointer;
    color: var( --text-color-black);
}

.dropdown-list {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    background: var(--saka-color);
    border-radius: 16px;
    margin-top: 5px;
    padding: 10px;
    z-index: 100;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
}

.color-circle {
    width: 20px;
    height: 20px;
    border-radius: 50%;
    cursor: pointer;
    transition: transform 0.2s;
}

.color-circle:hover {
    transform: scale(1.1);
}

.strel {
    font-size: 12px;
}
</style>