<template>
    <div class="order-block">
        <div class="order-content">
            <p class="order-title">
                Фабрика «Saka Tekstil» осуществляет прокрас <br>текстиля на заказ на самых выгодных условиях
            </p>
            <p class="order-subtitle">
                Просто оставьте заявку на сайте и мы свяжемся с вами в ближайшее время
            </p>
        </div>
        
        <div class="order-form">
            <input type="text" placeholder="Ваше имя" class="order-input">
            <input type="tel" placeholder="+7 (__) __.__-__" class="order-input">
            <input type="email" placeholder="Ваш E-mail" class="order-input">
            
            <Button theme="full" text="Отправить" icon="/src/assets/images/arrow.png" class="order-button"/>
        </div>
         <p class="order-agreement">
                Нажмите на кнопку вы даете свое согласие на обработку персональных данных. Гарантируем! Спам не будет!
        </p>
    </div>
</template>

<script>
import Button from '@/components/ui/Button.vue'

export default {
  components: {
    Button
  }
}
</script>

<style scoped>

.order-block {
    background-color: var(--color-dark-blue);
    width: 1160px;
    height: 330px;
    border-radius: 20px;
    margin: 50px 0px 50px 160px;
}

.order-title {
    font-size: var(--text-2xl);
    font-family: var(--font-family);
    color: var(--text-color);
    text-align: center;
    margin-bottom: 0;
    padding-top: 60px;
    padding-bottom: 15px;
}

.order-subtitle {
    font-size: var(--text-lg);
    font-family: var(--font-family);
    color: var(--text-color);
    text-align: center;
    margin-top: 5px;
    margin-bottom: 10px;
}

.order-form {
    display: flex;
    flex-wrap: nowrap;
    margin: 30px 0px 0px 90px;
}

.order-input {
    width: 200px;
    background-color: var(--color-nav);
    border-radius: 8px;
    font-family: var(--font-family);
    font-size: var(--text-sm);
    border: none;
    outline: none;
    margin-right: 20px;
    padding: 15px;
    color: white;
}

.order-input::placeholder {
    color: rgba(255, 255, 255, 0.7);
}

.order-button {
    height: 50px;
}

.order-agreement {
    font-size: var(--text-xs);
    color: var(--text-color);
    margin-top: 20px;
    text-align: center;
    font-family: var(--font-family);
}

@media (max-width: 768px) {
    .order-block {
        flex-direction: column;
        padding: 30px;
        gap: 40px;
    }
}
</style>