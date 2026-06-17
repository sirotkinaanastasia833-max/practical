<template>
  <div class="slider">
    <div class="slide">
      <div class="slide-content">
        <p class="slide-title">
          Здесь будет слайдер <br>с различными акциями <br>или <a href="">специальными <br>предложениями</a>
        </p>
        <div class="title-counter">{{ String(currentIndex + 1).padStart(2, '0') }}/05</div>
        <Button theme="full" text="Подробнее" icon="/src/assets/images/arrow.png"/>
      </div>
      
      <div class="dashes">
        <span 
          v-for="(slide, index) in slides" 
          :key="index"
          class="dash"
          :class="{ active: currentIndex === index }"
          @click="currentIndex = index"
        ></span>
      </div>
      <img src="./../../assets/images/women.png" alt="">
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Button from '@/components/ui/Button.vue'

const currentIndex = ref<number>(0)
const slides = ref<number[]>([1, 2, 3, 4, 5])

const prev = (): void => {
  currentIndex.value--
  if (currentIndex.value < 0) {
    currentIndex.value = 4
  }
}

const next = (): void => {
  currentIndex.value++
  if (currentIndex.value > 4) {
    currentIndex.value = 0
  }
}
</script>

<style scoped lang="scss">
.slider {
  position: relative;
  width: 1040px;
  margin: 50px auto auto 220px;
}

.slide {
  position: relative;
  width: 100%;
  min-height: 300px;
  background: var(--color-dark-blue);
  border-radius: 10px;
  padding: 40px;
  transition: background 0.3s;
  display: flex;
  flex-wrap: nowrap;

  img {
    margin-bottom: -180px;
    margin-top: -100px;
    width: 427px;
    height: 460px;
    margin-left: 100px;
  }
}

.slide-content {
  color: var(--text-color);
  display: flex;
  flex-direction: column;

  p {
    font-size: var(--text-3xl);
    font-family: var(--font-family);
  }

  a {
    color: var(--dark-gold);
    text-decoration: none;
  }
}

.slide-title {
  margin: 6px 0px 0px 45px;
}

.title-counter {
  margin-left: 65%;
  margin-top: 120px;
  font-family: var(--font-family);
  font-size: var(--text-base);
  letter-spacing: 3px;
}

:deep(.btn) {
  margin-left: 45px;
  margin-top: -115px;
}

.dashes {
  position: absolute;
  bottom: 40px;
  left: 17%;
  transform: translateX(-50%);
  display: flex;
  gap: 12px;
  z-index: 5;
}

.dash {
  width: 30px;
  height: 4px;
  background: rgba(255, 255, 255, 0.5);
  cursor: pointer;
  transition: all 0.3s;
  border-radius: 2px;

  &.active {
    background: var(--dark-gold);
    width: 40px;
  }

  &:hover {
    background: var(--dark-gold);
  }
}
</style>