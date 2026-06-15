<template>
    <div class="filter_wrapper">
        <div class="filter_first">
            <h1 class="title_filter">ФИЛЬТРЫ</h1>
            <div class="circle"><span class="three">3</span></div>
        </div>
        <div class="filter_second">
            <h1 class="title_filter_second">СБРОСИТЬ</h1>
            <span class="crest">X</span>
        </div>
        <div class="wrapper_sort">
            <h1 class="title_filter_second">СОРТИРОВКА:</h1>
            <div class="dropdown">
                <div class="dropdown-header" @click="isOpen = !isOpen">
                    {{ selected }}
                    <span>{{ isOpen ? '^' : 'v' }}</span>
                </div>
                <div class="dropdown-list" v-if="isOpen">
                    <div 
                        v-for="option in options" 
                        :key="option"
                        @click="select(option)"
                        class="dropdown-item"
                    >
                        {{ option }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const isOpen = ref(false)
const selected = ref('По новизне')

const options = ['По новизне', 'По популярности', 'Цена ниже']

const select = (option: string) => {
    selected.value = option
    isOpen.value = false
}
</script>

<style scoped lang="scss">
    .circle{
        width: 20px;
        height: 20px;
        background-color: var(--dark-gold);
        border-radius: 20px;
        margin: 7px 0px 0px 5px;
    }
    .three{
        color: var(--text-color);
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: var(--text-xs);
        font-family: var(--font-family);
        padding-top: 3px;
    }
    .filter_first{
        display: flex;
        flex-wrap: nowrap;
    }
    .title_filter{
        font-size: var(--text-sm);
        font-family: var(--font-family);
        color: var(--text-color-black);
    }
    .filter_wrapper{
        margin-left: 220px;
        display: flex;
        flex-wrap: nowrap;
        gap: 70px;
    }

    .crest{
        margin: 7px 0px 0px 5px;
        color: var(--secondary);
        display: flex;
        justify-content: center;
        font-size: var(--text-xs);
        font-family: var(--font-family);
        padding-top: 3px;
    }
    .filter_second{
        display: flex;
        flex-wrap: nowrap;
    }
    .title_filter_second{
        font-size: var(--text-sm);
        font-family: var(--font-family);
        color: var(--secondary);
    }
    .filter_wrapper{
        margin-left: 220px;
    }

    .sort-dropdown {
    position: relative;
    width: 200px;
}

.wrapper_sort{
    font-family: var(--font-family);
    display: flex;
    flex-wrap: nowrap;
}
.dropdown {
    position: relative;
    width: 150px;
    margin-top: -3px;
}

.dropdown-header {
    padding: 10px;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    border-radius: 8px;
    color: var(--text-color-black);
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