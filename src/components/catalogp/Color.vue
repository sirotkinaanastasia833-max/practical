<script setup lang="ts">
import { ref } from 'vue'
interface ColorOption {
    color: string
    name: string
}
const props = defineProps<{
    colors: ColorOption[]
    placeholder?: string
}>()
const isOpen = ref(false)
const selectedName = ref('')
const selectedColor = ref('')
const selectColor = (color: ColorOption) => {
    selectedName.value = color.name
    selectedColor.value = color.color
    isOpen.value = false
}
</script>

<template>
    <div class="color-dropdown">
        <div class="dropdown-header" @click="isOpen = !isOpen">
            <div class="selected-display">
                <div v-if="selectedColor" class="selected-circle" :style="{ backgroundColor: selectedColor }"></div>
                <span>{{ selectedName || placeholder || 'Цвет' }}</span>
            </div>
            <span class="strel">{{ isOpen ? '^' : 'v' }}</span>
        </div>
        
        <div class="dropdown-list" v-if="isOpen">
            <div 
                v-for="colorOption in colors" 
                :key="colorOption.color"
                class="dropdown-item"
                @click="selectColor(colorOption)">
                <div class="color-circle" :style="{ backgroundColor: colorOption.color }"></div>
                <span>{{ colorOption.name }}</span>
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
    padding: 20px;
    border-radius: 16px;
    margin-top: 10px;
    font-size: var(--text-xs);
}

.dropdown-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    cursor: pointer;
}

.selected-display {
    display: flex;
    align-items: center;
    gap: 10px;
}

.selected-circle {
    width: 20px;
    height: 20px;
    border-radius: 50%;
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
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.dropdown-item {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 8px;
    cursor: pointer;
    border-radius: 8px;
}


.color-circle {
    width: 20px;
    height: 20px;
    border-radius: 50px;
}

.strel {
    font-size: 12px;
}
</style>