<template>
    <Container>
        <div class="wrapper_container_footer">
            <div class="container_footer">
                <Logo class="logo"/>
                <div class="list_wrapper">
                    <div class="list_nav">
                        <h1 class="title_nav">Навигация</h1>
                        <li class="li_nav">
                            <ul class="ul_nav">Каталог</ul>
                            <ul class="ul_nav">О компании</ul>
                            <ul class="ul_nav">Новости</ul>
                            <ul class="ul_nav">Доставка и оплата</ul>
                            <ul class="ul_nav">Контакты</ul>
                            <ul class="ul_nav">Корзина</ul>
                        </li>
                    </div>
                    <div class="list_nav">
                        <h1 class="title_nav">Информация</h1>
                        <li class="li_nav">
                            <ul class="ul_nav">Помощь</ul>
                            <ul class="ul_nav">Блог</ul>
                            <ul class="ul_nav">Вопрос-ответ</ul>
                            <ul class="ul_nav">Политика конфиденциальности</ul>
                            <ul class="ul_nav">Карта сайта</ul>
                        </li>
                    </div>
                </div>
                <div class="email">
                    <h1 class="email_title">Следите за новостями</h1>
                    <div class="wrapper_email">
                        <input type="email" class="input_email" placeholder="Ваш E-mail">
                        <Button theme="text" text="Отправить" class="btn_email"/>
                    </div>
                </div>
                <div class="container_number">
                    <div><img src="./../../assets/images/Phone.png" alt="" class="number_image"></div>
                    <span class="telephone">+90 212 547 08 26</span>
                </div>
                <div class="network">
                    <h1 class="network_title">Напишите нам, <br>мы онлайн:</h1>
                    <div class="network_img">
                        <img src="./../../assets/images/VK.png" alt="" class="img_net">
                        <img src="./../../assets/images/whatsApp.png" alt="" class="img_net">
                        <img src="./../../assets/images/telegram.png" alt="" class="img_net">
                        <img src="./../../assets/images/instagram.png" alt="" class="img_net">
                    </div>
                </div>
                <p class="p">Copyright © 2023 Сака Текстиль. Все права защищены.</p>
            </div>
        </div>
    </Container>
</template>

<script setup lang="ts">
import Logo from '@/components/ui/Logo.vue';
import Button from '@/components/ui/Button.vue';
import Container from '../layout/Container.vue';
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;

.wrapper_container_footer {
    display: flex;
    justify-content: center;
    max-width: 100%;
}

.container_footer {
    max-width: 100%;
    max-height: 474px;
    background-color: var(--color-dark-blue);
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
    grid-template-rows: auto auto auto auto auto auto;
    grid-template-areas:
        "logo nav nav email email"
        ". nav nav email email"
        ". nav nav . Number"
        ". nav nav . ."
        ". . . . ."
        "network network . p p";

    @include tablet {
        max-width: 698px;
        max-height: 732px;
        display: grid;
        padding: 10px;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        grid-template-rows: 140px auto auto auto auto;
        grid-template-areas:
            "logo nav nav ."
            ". nav nav ."
            "email email email email"
            "Number Number . ."
            "network network network p";
    }
    @include mobile {
        max-width: 360px;
        max-height: 1070px;
        display: flex;
        flex-direction: column;
    }
}

.logo {
    grid-area: logo;
    padding: 40px 0px 0px 70px;

    @include tablet {
        padding: 40px 0px 0px 20px;
    }
}

.list_wrapper {
    display: flex;
    flex-wrap: nowrap;
    grid-area: nav;
    padding: 50px 0px 50px 0px;

    @include tablet {
        margin-left: 0;
        padding: 50px 0px 50px 0px;
    }
    @include mobile {
        display: flex;
        flex-wrap: wrap;
        padding-left: 10px;
    }
}

.list_nav {
    &:last-child {
        @include tablet {
            margin-left: 40px;
        }
        @include mobile {
            margin-left: 0px;
            margin-top: 10px;
        }
    }
}

.li_nav {
    list-style: none;
    color: var(--text-color);
    font-size: var(--text-sm);
    font-family: var(--font-family);
    margin-right: 30px;

    @include tablet {
        margin-right: 20px;
    }
}

.ul_nav {
    margin-bottom: 8px;
    cursor: pointer;
    
    &:hover {
        color: var(--dark-gold);
    }
}

.title_nav {
    color: var(--text-color);
    font-size: var(--text-base);
    font-family: var(--font-family);
    margin: 0px 0px 20px 40px;

    @include tablet {
        margin: 0px 0px 20px 0px;
    }
}

.email {
    grid-area: email;
    padding: 35px 0px 0px 0px;
    margin-right: 40px;

    @include tablet {
        margin-left: 20px;
        margin-right: 20px;
        padding: 35px 0px 20px 0px;
    }
}

.network {
    grid-area: network;
    gap: 20px;
    display: flex;
    flex-wrap: nowrap;
    margin: 10px 0px 50px 100px;

    @include tablet {
        margin: 10px 0px 30px 20px;
        gap: 15px;
        flex-wrap: wrap;
    }
}

.p {
    grid-area: p;
    font-family: var(--font-family);
    font-size: var(--text-sm);
    color: var(--secondary);
    margin: 30px 0px 0px 70px;

    @include tablet {
        margin: 10px 6px 20px 20px;
    }
}

.container_number {
    grid-area: Number;
    display: flex;
    flex-wrap: nowrap;

    @include tablet {
        padding-left: 20px;
    }
}

.number_image {
    margin-top: 30px;
}

.telephone {
    margin-top: 30px;
    color: var(--text-color);
    font-size: var(--text-xl);
    margin-left: 10px;
}

.wrapper_email {
    display: flex;
    align-items: center;
    position: relative;
    padding-top: 10px;

    @include tablet {
        flex-wrap: wrap;
    }
}

.input_email {
    width: 440px;
    height: 55px;
    background-color: var(--color-nav);
    border-radius: 30px;
    border: none;
    padding: 0 200px 0 30px;
    color: var(--text-color);
    font-family: var(--font-family);
    font-size: 14px;

    &::placeholder {
        color: rgba(255, 255, 255, 0.5);
    }

    &:focus {
        outline: 2px solid var(--dark-gold);
    }

    @include tablet {
        width: 100%;
        max-width: 440px;
        padding: 0 180px 0 30px;
    }
}

.btn_email {
    position: absolute;
    right: 0;
    width: 182px;
    height: 55px;
    border-radius: 30px;
    border: none;
    cursor: pointer;
    background-color: var(--dark-gold);
    color: var(--text-color-black);
    font-family: var(--font-family);
    font-size: 16px;
    font-weight: 600;
    transition: all 0.3s ease;

    &:hover {
        transform: scale(1.02);
    }

    @include tablet {
        width: 160px;
    }
}

.email_title {
    font-family: var(--font-family);
    font-size: var(--text-base);
    color: var(--text-color);
}

.network_title {
    font-family: var(--font-family);
    font-size: var(--text-base);
    color: var(--text-color);
}

.network_img {
    margin-top: 15px;
}

.img_net {
    margin-left: 10px;
    cursor: pointer;
    transition: all 0.3s ease;

    &:hover {
        transform: scale(1.1);
    }
}
</style>