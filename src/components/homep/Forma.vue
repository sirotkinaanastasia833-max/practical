<template>
    <Container>
        <div class="form_wrapper">
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
        </div>
    </Container>
</template>

<script>
import Button from '@/components/ui/Button.vue'
import Container from '../layout/Container.vue';

export default {
  components: {
    Button
  }
}
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;

.form_wrapper{
    display: flex;
    justify-content: center;
}

.order-block {
    background-color: var(--color-dark-blue);
    width: 1160px;
    height: 330px;
    border-radius: 20px;
    @include tablet {
        flex-direction: column;
        width: 565px;
        margin: 50px 0px 50px 0px;
        height: 600px;
    }
    @include mobile {
        flex-direction: column;
        width: 360px;
        margin: 50px 0px 50px 0px;
        height: 630px;
    }
}

.order-title {
    font-size: var(--text-2xl);
    font-family: var(--font-family);
    color: var(--text-color);
    text-align: center;
    margin-bottom: 0;
    padding-top: 60px;
    padding-bottom: 15px;
    @include tablet {
          width: 560px;
        }
    @include mobile {
          width: 300px;
          font-size: var(--text-xl);
          padding-left: 30px;
    }
}

.order-subtitle {
    font-size: var(--text-lg);
    font-family: var(--font-family);
    color: var(--text-color);
    text-align: center;
    margin-top: 5px;
    margin-bottom: 10px;
    @include mobile {
        width: 300px;
        font-size: var(--text-base);
        padding-left: 30px;
    }
}

.order-form {
    display: flex;
    flex-wrap: nowrap;
    margin: 30px 0px 0px 90px;
    @include tablet {
        flex-direction: column;
        gap: 15px;
    }
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
    @include tablet {
        width: 500px;
        height: 30px;
        margin-left: -70px;
    }
    @include mobile {
        width: 300px;
        height: 30px;
        margin-left: -70px;
        border-radius: 16px;
    }
}

.order-input::placeholder {
    color: rgba(255, 255, 255, 0.7);
}

.order-button {
    height: 50px;
    @include tablet {
        width: 530px;
        height: 50px;
        margin-left: -70px;
    }
    @include mobile {
        width: 330px;
        height: 50px;
        margin-left: -70px;
    }
    
}

.order-agreement {
    font-size: var(--text-xs);
    color: var(--text-color);
    margin-top: 20px;
    text-align: center;
    font-family: var(--font-family);
    @include tablet {
        display: none;
    }
}

@media (max-width: 768px) {
    .order-block {
        flex-direction: column;
        padding: 30px;
        gap: 40px;
    }
}
</style>