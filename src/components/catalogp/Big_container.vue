<template>
    <Container>
        <div class="wrapper_big_container">
            <div class="wrapper_big">
                <div class="box_filter">
                    <Container_filter class="Container_filter"/>
                    <Dropdown :options="['Плотные', 'Не плотные']"  placeholder="Тип полотна" class="Container_filter" />
                    <Dropdown :options="['Кулирная гладь', 'Рибана', 'Пике', 'Интерлок', 'Футер 2-х нитка', 'Футер 3-х нитка', 'Кашкорсе к 2х нитке', 'Кашкорсе к 3х нитке', 'Double Face']"  placeholder="Качество" class="Container_filter" />
                    <ColorDropdown :colors="colors" placeholder="Цвет" />
                    <Color 
                        :colors="colorss" 
                        placeholder="Цвет"
                    />
                </div>
                <Catalog/>
            </div>
        </div>
    </Container>
</template>

<script setup lang="ts">
import Container_filter from '@/components/catalogp/Container_filter.vue';
import Catalog from '@/components/catalogp/Catalog.vue';
import Dropdown from '@/components/catalogp/Dropdown.vue';
import ColorDropdown from '@/components/catalogp/ColorDropdown.vue';
const colors = ['#F5DC41', '#007C7A', '#263669', '#4A7AB8', '#B2092C', '#B5A0C9', '#FC8B23', '#C8C8C8', '#DBC08D', '#FFFFFF', '#B5A0C9', '#FC8B23', '#BFA470', '#F5DC41', '#007C7A', '#FFFFFF']
import Color from '@/components/catalogp/Color.vue';
const colorss = [
    { color: '#F5DC41', name: 'Желтый' },
    { color: '#007C7A', name: 'Темно-зеленый' },
    { color: '#263669', name: 'Синий' },
    { color: '#4A7AB8', name: 'Темно-голубой' },
    { color: '#B2092C', name: 'Красно-пурпурно-бордовый' },
    { color: '#B5A0C9', name: 'Нежненький' }
]
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
.box_filter{
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: center;
    padding: 30px;
    @include tablet{
        display: none;
    }
    @include mobile{
            display: none;
        }
}
.wrapper_big_container{
    display: flex;
    justify-content: center;
}
.wrapper_big{
    display: flex;
    flex-wrap: nowrap;
}
.Container_filter{
    display: flex;
    justify-content: center;
}
</style>