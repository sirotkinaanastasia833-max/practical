<template>
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
</template>
<script setup lang="ts">
import Logo from '@/components/ui/Logo.vue';
import Button from '@/components/ui/Button.vue';
</script>
<style scoped lang="scss">
    .container_footer{
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
    }
    .logo{
        grid-area: logo;
        padding: 50px 30px 80px 200px;
    }
    .list_wrapper{
        display: flex;
        flex-wrap: nowrap;
        grid-area: nav;
        padding: 50px 0px 50px 0px;
    }
    .li_nav{
        list-style: none;
        color: var(--text-color);
        font-size: var(--text-sm);
        font-family: var(--font-family);
        margin-right: 30px;
    }
    .title_nav{
        color: var(--text-color);
        font-size: var(--text-base);
        font-family: var(--font-family);
        margin: 0px 0px 20px 40px;
    }
    .email{
        grid-area: email;
        padding: 35px 0px 0px 0px;
        margin-right: 40px;
    }
    .network{
        grid-area: network;
        gap: 20px;
        display: flex;
        flex-wrap: nowrap;
        margin: 10px 0px 50px 210px;
    }
    .p{
        grid-area: p;
        font-family: var(--font-family);
        font-size: var(--text-sm);
        color: var(--secondary);
        margin: 30px 0px 0px 70px;
    }
    .number_wrapper{
        display: flex;
        flex-wrap: nowrap;
    }
    .number_image{
        margin-top: 30px;
    }
    .container_number{
        grid-area: Number;
        display: flex;
        flex-wrap: nowrap;
    }
    .telephone{
        margin-top: 30px;
        color: var(--text-color);
        font-size: var(--text-xl);
    }
    .input_email{
        width: 440px;
        height: 55px;
        background-color: var(--color-nav);
        border-radius: 30px;
        border: none;
        padding-left: 30px;
    }
    .email_title{
        font-family: var(--font-family);
        font-size: var(--text-base);
        color: var(--text-color);
    }
    .btn_email{
        width: 182px;
        height: 55px;
        margin-left: 300px;
        position: absolute;
    }
    .wrapper_email{
        display: flex;
        flex-wrap: nowrap;
        padding-top: 10px;
    }
    .network_title{
        font-family: var(--font-family);
        font-size: var(--text-base);
        color: var(--text-color);
    }
    .network_img{
        margin-top: 15px;
    }
    .img_net{
        margin-left: 10px;
    }
</style>