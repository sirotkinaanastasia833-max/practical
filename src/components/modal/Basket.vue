<template>
  <div v-if="isVisible" class="modal-overlay" @click.self="closeModal">
    <div class="modal-container">
      <button @click="closeModal" class="close-btn"><img src="./../../assets/images/X-mod.png" alt=""/></button>
      
      <h2 class="modal-title">Корзина</h2>
      
      <div class="cart-items">
        <div class="cart-item">
          <img src="./../../assets/images/modal-img.png" alt="Товар" class="item-image"/>
          <div class="item-info">
            <span class="item-name">Футер 2-х нитка диагональ</span>
            <div class="item-bottom">
              <button class="qty-btn">-</button>
              <span class="qty-number">3</span>
              <button class="qty-btn">+</button>
            </div>
          </div>
          <div class="item-right">
            <span class="item-price">450₽</span>
            <button class="delete-btn">✕</button>
          </div>
        </div>
        
        <div class="cart-item">
          <img src="./../../assets/images/modal-img.png" alt="Товар" class="item-image"/>
          <div class="item-info">
            <span class="item-name">Футер 2-х нитка диагональ</span>
            <div class="item-bottom">
              <button class="qty-btn">-</button>
              <span class="qty-number">16</span>
              <button class="qty-btn">+</button>
            </div>
          </div>
          <div class="item-right">
            <span class="item-price">4650₽</span>
            <button class="delete-btn">✕</button>
          </div>
        </div>
        
        <div class="cart-item">
          <img src="./../../assets/images/modal-img.png" alt="Товар" class="item-image"/>
          <div class="item-info">
            <span class="item-name">Футер 2-х нитка диагональ</span>
            <div class="item-bottom">
              <button class="qty-btn">-</button>
              <span class="qty-number">1</span>
              <button class="qty-btn">+</button>
            </div>
          </div>
          <div class="item-right">
            <span class="item-price">305 005₽</span>
            <button class="delete-btn">✕</button>
          </div>
        </div>
      </div>
      
      <hr class="divider"/>
      
      <form class="cart-form">
        <div class="form-group">
          <div class="input-wrapper">
            <img src="./../../assets/images/Envelope.png" alt="E-Mail" class="input-icon"/>
            <input type="email" placeholder="E-Mail" class="form-input"/>
          </div>
        </div>
        
        <div class="form-group">
          <div class="input-wrapper">
            <img src="./../../assets/images/Phone-modal.png" alt="Телефон" class="input-icon"/>
            <input type="tel" placeholder="+7 (____) ____-____-____" class="form-input"/>
          </div>
        </div>
      </form>
      
      <hr class="divider"/>
      
      <Button theme="full" text="Оформить заказ" icon="/src/assets/images/ShoppingCart.png" class="submit-btn"/>
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
    padding: 40px 35px 30px;
    max-width: 480px;
    width: 100%;
    position: relative;
    box-shadow: 0 20px 60px rgba(0, 0, 0, 0.2);
}

.close-btn {
    position: absolute;
    top: 12px;
    right: 16px;
    background: none;
    border: none;
    cursor: pointer;
    padding: 4px 8px;
}

.modal-title {
    font-size: 24px;
    font-weight: 600;
    color: var(--text-color-black);
    text-align: left;
    margin: 0 0 30px 0;
    font-family: var(--font-family);
}

.cart-items {
    display: flex;
    flex-direction: column;
    gap: 15px;
    margin-bottom: 25px;
}

.cart-item {
    display: flex;
    align-items: center;
    gap: 12px;
    background-color: var(--text-color);
    padding: 0 12px;
    height: 60px;
    border-radius: 8px;
}

.item-image {
    width: 50px;
    height: 50px;
    object-fit: cover;
    border-radius: 8px;
    flex-shrink: 0;
}

.item-info {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 4px;
}

.item-name {
    font-size: 14px;
    color: var(--text-color-black);
    font-family: var(--font-family);
}

.item-bottom {
    display: flex;
    align-items: center;
}

.qty-btn {
    width: 18px;
    height: 18px;
    border: none;
    border-radius: 50%;
    background: var(--saka-color);
    color: var(--text-color-black);
    font-size: 11px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0;
    line-height: 1;
}

.qty-number {
    font-size: 12px;
    color: var(--text-color-black);
    font-family: var(--font-family);
    min-width: 14px;
    text-align: center;
    margin: 0 4px;
}

.item-right {
    display: flex;
    align-items: center;
    gap: 8px;
    flex-shrink: 0;
}

.item-price {
    font-size: 14px;
    font-weight: 600;
    color: var(--text-color-black);
    font-family: var(--font-family);
}

.delete-btn {
    background: none;
    border: none;
    cursor: pointer;
    font-size: 14px;
    color: var(--text-color-black);
    opacity: 0.2;
    padding: 4px;
}

.divider {
    border: none;
    border-top: 1px solid #e8e8e8;
    margin: 0 0 25px 0;
}

.cart-form {
    display: flex;
    flex-direction: column;
    gap: 15px;
    margin-bottom: 25px;
}

.form-group {
    width: 100%;
}

.input-wrapper {
    position: relative;
    width: 100%;
}

.input-icon {
    position: absolute;
    left: 14px;
    top: 50%;
    transform: translateY(-50%);
    width: 18px;
    height: 18px;
    pointer-events: none;
}

.form-input {
    width: 100%;
    height: 59px;
    padding: 14px 16px 14px 44px;
    border: none;
    border-radius: 8px;
    font-size: 15px;
    font-family: var(--font-family);
    color: var(--text-color-black);
    background: var(--text-color);
    box-sizing: border-box;
    outline: none;
    opacity: 0.5;
}

.submit-btn {
    width: 100%;
    padding: 14px;
    border: none;
    font-size: 16px;
    font-weight: 600;
    font-family: var(--font-family);
    cursor: pointer;
}
</style>