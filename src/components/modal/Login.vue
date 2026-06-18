<template>
  <div v-if="isVisible" class="modal-overlay" @click.self="closeModal">
    <div class="modal-container">
      <div class="modal-header">
        <button @click="closeModal" class="close-btn"><img src="./../../assets/images/X-mod.png" alt=""></button>
        <h2>Вход</h2>
      </div>
      <div class="modal-body">
        <div class="input-wrapper">
          <img src="./../../assets/images/user-modal.png" alt="Логин" class="input-icon"/>
          <input type="text" placeholder="Логин"/>
        </div>
        <div class="input-wrapper">
          <img src="./../../assets/images/Eye.png" alt="Пароль" class="input-icon"/>
          <input type="password" placeholder="Пароль"/>
        </div>
      </div>
      <div class="btn_user">
        <Button theme="text" text="Войти" class="button_us"/>
      </div>
      <div class="title_modal">
        <a href="#">Забыли пароль?</a>
        <p>Зарегистрироваться</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Button from '@/components/ui/Button.vue';

interface Props {
  isVisible: boolean
}

const props = defineProps<Props>()
const emit = defineEmits<{
  (e: 'close'): void
}>()

const closeModal = (): void => {
  emit('close')
}
</script>

<style scoped lang="scss">
.modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.6);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}
.modal-container {
    background: var(--saka-color);
    border-radius: 12px;
    padding: 30px;
    width: 310px;
    max-width: 90%;
}
.modal-header {
    align-items: center;
    margin-bottom: 20px;
}
.close-btn {
    background: none;
    border: none;
    font-size: 24px;
    cursor: pointer;
    margin-top: -15px;
    margin-left: 240px;
}
.modal-body {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
    margin-bottom: 15px;
}
.input-wrapper {
    position: relative;
    width: 320px;
    max-width: 100%;
}
.input-icon {
    position: absolute;
    left: 12px;
    top: 50%;
    transform: translateY(-50%);
    width: 20px;
    height: 20px;
}
.modal-body input {
    padding: 10px 10px 10px 42px;
    border: none;
    border-radius: 12px;
    font-size: 16px;
    width: 320px;
    height: 55px;
    box-sizing: border-box;
    outline: none;
    opacity: 0.5;
}
.btn_user {
    display: flex;
    justify-content: center;
}
.title_modal a {
    display: flex;
    justify-content: center;
    font-family: var(--font-family);
    color: var(--text-color-black);
    margin-top: 20px;
}
.title_modal p {
    display: flex;
    justify-content: center;
    color: var(--dark-gold);
    font-family: var(--font-family);
    cursor: pointer;
}
.button_us {
    width: 240px;
    max-width: 100%;
    height: 50px;
}
h2 {
    font-family: var(--font-family);
    display: flex;
    justify-content: center;
}
</style>