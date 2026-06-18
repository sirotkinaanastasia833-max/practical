<template>
  <Container>
    <div class="wrapper_slider">
      <div class="slider">
        <div class="slide">
          <div class="slide-content">
            <p class="slide-title">Здесь будет слайдер с различными акциями или <a href="">специальными предложениями</a></p>
            <div class="title-05">01/05</div>
            <Button theme="full" text="Подробнее" icon="/src/assets/images/arrow.png"/>
          </div>
          <img src="./../../assets/images/women.png" alt="">
        </div>
      </div>
    </div>
  </Container>
</template>
<script setup lang="ts">
import Button from '@/components/ui/Button.vue'
import Container from '../layout/Container.vue';
</script>
<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
.slider {
  margin-top: 60px;
}
.wrapper_slider{
  display: flex;
  justify-content: center;
}
.slide {
  position: relative;
  width: 100%;
  min-height: 380px;
  background: var(--color-dark-blue);
  border-radius: 10px;
  padding: 40px;
  transition: background 0.3s;
  display: flex;
  flex-wrap: nowrap;
  @include tablet {
    max-width: 620px;
    min-height: 460px;
  }
  @include mobile {
    max-width: 300px;
    min-height: 618px;
  }
}
.slide-content {
  color: var(--text-color);
  display: flex;
  flex-direction: column;
}
.slide-title {
  margin: 6px 0px 0px 45px;
  font-weight: 600;
  width: 451px;
  @include tablet {
    width: 370px;
    height: 140px;
  }
}
.slide-content p {
  font-size: var(--text-3xl);
  font-family: var(--font-family);
  font-weight: 600;
  padding-left: 30px;
  @include tablet {
    font-size: var(--text-2xl);
    padding-top: 50px;
    letter-spacing: 7%;
    font-weight: 600;
    padding-left: 0px;
  }
  @include mobile {
    width: 247px;
    height: 96px;
    font-size: 18px;
    padding-top: 0px;
    margin: 0
  }
}
.slide-content img {
  max-width: 100%;
  border-radius: 10px;
  margin: 20px 0;
  box-shadow: 0 4px 15px rgba(0,0,0,0.2);
  @include tablet{

  }
}
.dashes {
  position: absolute;
  bottom: 40px;
  left: 17%;
  transform: translateX(-50%);
  display: flex;
  gap: 12px;
  z-index: 5;
  @include tablet {
    margin-left: 50px;
  }
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
  @include tablet {
    margin-left: -120px;
    margin-top: -20px;
    width: 427px;
    height: 460px;
    z-index: 1;
  }
  @include mobile {
    margin-left: -350px;
    margin-top: 244px;
    width: 344px;
    height: 348px;
    z-index: 1;
  }
}
.title-05 {
  margin-left: 65%;
  margin-top: 120px;
  font-family: var(--font-family);
  font-size: var(--text-base);
  letter-spacing: 3px;
  @include tablet {
    margin-top: 223px;
  }
  @include mobile {
    margin-top: 200px;
    margin-left: 20px;
  }
}
.slide-content :deep(.btn) {
  margin-left: 70px;
  margin-top: -115px;
  @include tablet {
    margin-left: 45px;
    margin-top: -183px;
  }
  @include mobile {
    z-index: 2;
    margin-top: -200px;
    margin-left: -21px;
  }
}
.Button_carusel{
  @include tablet {
    margin-top: -130px;
    z-index: 2;
  }
  @include mobile {
    margin-top: -130px;
    z-index: 2;
  }
}
</style>