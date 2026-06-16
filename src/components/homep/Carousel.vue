<template>
  <div class="slider">
    <div class="slide">
      <div v-if="currentIndex === 0" class="slide-content">
        <p class="slide-title">Здесь будет слайдер <br>с различными акциями <br>или <a href="">специальными <br>предложениями</a></p>
        <div class="title-05">01/05</div>
        <Button theme="full" text="Подробнее" icon="/src/assets/images/arrow.png"/>
      </div>
      <div v-if="currentIndex === 1" class="slide-content">
        <p class="slide-title">Здесь будет слайдер <br>с различными акциями <br>или <a href="">специальными <br>предложениями</a></p>
        <div class="title-05">02/05</div>
        <Button theme="full" text="Подробнее" icon="/src/assets/images/arrow.png"/>
      </div>
      <div v-if="currentIndex === 2" class="slide-content">
        <p class="slide-title">Здесь будет слайдер <br>с различными акциями <br>или <a href="">специальными <br>предложениями</a></p>
        <div class="title-05">03/05</div>
        <Button theme="full" text="Подробнее" icon="/src/assets/images/arrow.png"/>
      </div>
      <div v-if="currentIndex === 3" class="slide-content">
        <p class="slide-title">Здесь будет слайдер <br>с различными акциями <br>или <a href="">специальными <br>предложениями</a></p>
        <div class="title-05">04/05</div>
        <Button theme="full" text="Подробнее" icon="/src/assets/images/arrow.png"/>
      </div>
      <div v-if="currentIndex === 4" class="slide-content">
        <p class="slide-title">Здесь будет слайдер <br>с различными акциями <br>или <a href="">специальными <br>предложениями</a></p>
        <div class="title-05">05/05</div>
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

<script>
import Button from '@/components/ui/Button.vue'

export default {
  components: {
    Button
  },
  data() {
    return {
      currentIndex: 0,
      slides: [1, 2, 3, 4, 5] 
    }
  },
  methods: {
    prev() {
      this.currentIndex--;
      if (this.currentIndex < 0) {
        this.currentIndex = 4;
      }
    },
    next() {
      this.currentIndex++;
      if (this.currentIndex > 4) {
        this.currentIndex = 0;
      }
    }
  }
}
</script>

<style scoped>
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
}
.slide-content {
  color: var(--text-color);
  display: flex;
  flex-direction: column;
}
.slide-title {
  margin: 6px 0px 0px 45px;
  font-weight: 600;
}
.slide-content p {
  font-size: var(--text-3xl);
  font-family: var(--font-family);
  font-weight: 600;
}
.slide-content img {
  max-width: 100%;
  border-radius: 10px;
  margin: 20px 0;
  box-shadow: 0 4px 15px rgba(0,0,0,0.2);
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
}
.dash.active {
  background: var(--dark-gold);
  width: 40px;
}
.dash:hover {
  background: var(--dark-gold);
}
.slide-content a {
  color: var(--dark-gold);
  text-decoration: none;
}
.slide img {
  margin-bottom: -180px;
  margin-top: -100px;
  width: 427px;
  height: 460px;
  margin-left: 100px;
}
.title-05 {
  margin-left: 65%;
  margin-top: 120px;
  font-family: var(--font-family);
  font-size: var(--text-base);
  letter-spacing: 3px;
}

.slide-content :deep(.btn) {
  margin-left: 45px;
  margin-top: -115px;
}
</style>