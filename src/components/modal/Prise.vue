<template>
  <div v-if="isVisible" class="modal-overlay" @click.self="closeModal">
    <div class="modal-container">
      <button @click="closeModal" class="close-btn"><img src="./../../assets/images/X-modal.png" alt=""></button>
      
      <div class="modal-content">
        <div class="modal-left">
          <h2 class="modal-title">Заказать прайс-лист и каталог</h2>
          <p class="modal-subtitle">Оставьте заявку и получите образцы</p>
          
          <form class="modal-form">
            <div class="form-group">
               <div class="input-wrapper">
                 <img src="./../../assets/images/user-modal.png" alt="Имя" class="input-icon"/>
                 <input type="text" placeholder="Имя" class="form-input"/>
               </div>
            </div>
            
            <div class="form-group">
              <div class="input-wrapper">
                <img src="./../../assets/images/Envelope.png" alt="E-Mail" class="input-icon"/>
                <input type="email" placeholder="E-Mail" class="form-input"/>
              </div>
            </div>
            
            <div class="form-group">
              <div class="input-wrapper">
                <img src="./../../assets/images/Phone-modal.png" alt="Телефон" class="input-icon"/>
                <input type="tel" placeholder="+7 (____) __.__.____" class="form-input"/>
              </div>
            </div>
            
            <div class="form-group">
              <div class="input-wrapper">
                <img src="./../../assets/images/MapPin.png" alt="Адрес" class="input-icon"/>
                <input type="text" placeholder="Адрес доставки" class="form-input"/>
              </div>
            </div>
            
            <Button theme="text" text="Оставить заявку" class="submit-btn"/>
          </form>
          
          <p class="agreement-text">
            Нажимая на кнопку вы даете свое согласие на обработку персональных данных. Гарантируем! Спам не будет!
          </p>
        </div>
        
        <div class="modal-right">
          <img src="./../../assets/images/modal.png" alt="Образцы" class="modal-image"/>
        </div>
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
  padding: 20px;
}

.modal-container {
  background: var(--saka-color);
  border-radius: 16px;
  padding: 0;
  max-width: 960px;
  width: 100%;
  position: relative;
  overflow: hidden;
  height: 588px;
}

.close-btn {
  position: absolute;
  top: 12px;
  right: 16px;
  background: none;
  border: none;
  font-size: 24px;
  cursor: pointer;
  padding: 4px 8px;
  z-index: 10;

}

.modal-content {
  display: flex;
  gap: 0;
  align-items: stretch;
}

.modal-left {
  flex: 1;
  min-width: 0;
  padding: 40px 35px 30px;
}

.modal-right {
  width: 560px;
  height: 588px;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.modal-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.modal-title {
  font-size: 20px;
  font-weight: 600;
  color: var(--text-color-black);
  text-align: left;
  margin: 0 0 8px 0;
  font-family: var(--font-family);
}

.modal-subtitle {
  font-size: 14px;
  color: var(--text-color-black);
  text-align: left;
  margin: 0 0 30px 0;
  font-family: var(--font-family);
  font-weight: 300;
}

.modal-form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.form-group {
  width: 100%;
}

.input-wrapper {
  position: relative;
  width: 320px;
  max-width: 100%;
}

.input-icon {
  position: absolute;
  left: 14px;
  top: 50%;
  transform: translateY(-50%);
  width: 18px;
  height: 18px;
  pointer-events: none;
  transition: opacity 0.3s ease;
}

.form-input {
  width: 320px;
  max-width: 100%;
  padding: 14px 16px 14px 44px;
  border: none;
  border-radius: 8px;
  font-size: 15px;
  font-family: var(--font-family);
  color: var(--text-color-black);
  background: var(--text-color);
  box-sizing: border-box;
  outline: none;
  height: 55px;
}

.submit-btn {
  width: 320px;
  max-width: 100%;
  height: 50px;
}

.agreement-text {
  font-size: 12px;
  color: #888;
  text-align: left;
  margin: 18px 0 0 0;
  font-family: var(--font-family);
  line-height: 1.5;
}

.modal-form input{
    opacity: 0.5;
}
</style>