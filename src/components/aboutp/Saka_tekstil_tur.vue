<template>
    <Container>
        <div class="tekstil">
        <img src="./../../assets/images/Saka_tur.png" alt="" class="img_tek">
        <div class="tekstil_right">
            <p class="tekstil_title">
                Saka Tekstil - производство и продажа <br>турецкого трикотажного полотна
            </p>
            <div class="tekstil_li">
                <div class="tekstil_li_title">
                    Мы осуществляем продажу ткани от рулона и нарезку кашкорсе от 5%-20%
                </div>
            </div>
            <div class="tekstil_li">
                <div class="tekstil_li_title">
                    Наша команда следит за трендами в мире <br>трикотажа, мы постоянно 
                    обновляем наш <br>ассортимент и регулярно контролируем <br>наличие ткани на складе
                </div>
                <div class="tekstil_lit">
                    Мы предлагаем клиентам различные виды 
                    <br>трикотажных полотен высокого качества <br>более, чем в 45 цветовых вариациях
                </div>
            </div>
            <div class="circle_group">
                <div class="circle">
                <img src="./../../assets/icons/queen.svg" alt="" class="circle_img">
                <p class="tit_circle">30</p>
                <p class="title_circle">Лет на рынке <br>текстиля</p>
               </div>
            <div class="circle_right">
                <div class="circle">
                    <img src="./../../assets/icons/queen.svg" alt="" class="circle_img">
                    <p class="tit_circle">40+</p>
                    <p class="title_circle">Ассортимент <br>товаров <br>в наличии</p>
                </div>
            </div>
            <div class="circle">
                <img src="./../../assets/icons/queen.svg" alt="" class="circle_img">
                <p class="tit_circle">10 000+</p>
                <p class="title_circle">Клиентов <br>выбирают нашу <br>компанию</p>
            </div>
            </div>
        </div>
    </div>
    </Container>
</template>

<script setup>
import Container from '../layout/Container.vue';
// export default {
//   components: {
//     Button
//   }
// }
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
.tekstil{
    display: flex;
    flex-wrap: nowrap;
    color: var(--text-color-black);
    @include mobile{
        display: flex;
        flex-direction: column;
    }
}

.tekstil_li{
    font-size: var(--text-lg);
    font-family: var(--font-family);
}

a{
    text-decoration: none;
    color: var(--dark-gold);
}

.img_tek{
    @include tablet{
        width: 339px;
        height: 576px;
    }
    @include tablet{
        width: 330px;
        height: 576px;
    }
}

.tekstil_right img{
    margin-left: -45px;
}

.tekstil_right{
    margin-left: 120px;
    margin-top: 50px;
    @include tablet {
        margin-left: 30px;
    }
}

.tekstil_title{
    font-size: var(--text-2xl);
    font-family: var(--font-family);
    font-weight: 500;
    @include mobile{
        font-size: var(--text-xl);
        width: 300px;
    }

}
.tekstil_li_title{
    margin-top: 15px;
    font-family: var(--font-family);
    @include mobile{
        font-size: var(--text-sm);
        width: 300px;
    }
}



.custom-button {
    width: 300px !important;
    margin-top: 80px;
    @include tablet {
        margin-top: 40px;
        margin-bottom: 40px;
    }
}

.tekstil_lit{
    margin-top: 15px;
    font-family: var(--font-family);
    @include mobile{
        font-size: var(--text-sm);
        width: 300px;
    }
}

.circle{
    background-color: var(--saka-color);
    width: 160px;
    height: 160px;
    border-radius: 90px;
    text-align: center;
    margin-top: 40px;
    @include tablet{
        width: 180px;
        height: 180px;
    }
}

.title_circle{
    font-family: var(--font-family);
}

.tit_circle{
    margin-top: 20px;
    font-size: 32px;
    color: var(--dark-gold);
    font-family: var(--font-family);
}

.circle img{
    margin-bottom: -20px;
    margin-left: -2px;
}

.circle_group{
    display: flex;
    flex-wrap: nowrap;
    gap: 15px;
    @include tablet{
        display: flex;
        justify-content: center;
        z-index: 2;
    }
    @include mobile{
        display: flex;
        justify-content: center;
        flex-direction: column;
        padding-left: 20px;
    }
}
.circle_right{
    @include mobile{
        padding-left: 100px;
    }
}
</style>