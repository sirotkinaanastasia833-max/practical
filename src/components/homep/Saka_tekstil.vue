<template>
    <Container>
        <div class="tekstil">
        <img src="./../../assets/images/sakatekstil.png" alt="" class="tekstil_image">
        <div class="tekstil_right">
            <p class="tekstil_title">
                Saka Tekstil – для тех, кто хочет быстро 
                <br>и комфортно получать текстильную <br>продукцию <a href="">высокого качества 
                <br>по адекватной стоимости</a>
            </p>
            <div class="tekstil_li">
                <img src="./../../assets/images/saka_tire.png" alt="">
                <div class="tekstil_li_title">
                    Предоставляем возможность закупки<br>широкого ассортимента: футер, 
                    кулирка,<br>джакарт, флис, рибана и многое другое…
                </div>
            </div>
            <div class="tekstil_li_bottom">
                <div class="tekstil_li">
                    <img src="./../../assets/images/saka_tire.png" alt="">
                    <div class="tekstil_li_title">
                        Наша компания является надежным <br>поставщиком и 
                        производителем турецкого <br>трикотажного полотна по всему миру
                    </div>
                </div>
            </div>
            <Button theme="full" text="Смотреть каталог" icon="/src/assets/images/arrow.png" class="custom-button"/> 
       </div>
    </div>
    </Container>
</template>

<script setup>
import Button from '@/components/ui/Button.vue'
import Container from '../layout/Container.vue';
</script>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;

.tekstil{
    background-color: var(--saka-color);
    display: flex;
    flex-wrap: nowrap;
    padding: 0 40px;
    
    @include tablet {
        max-width: 100%;
        height: auto;
        flex-direction: column-reverse;
        align-items: center;
        padding-left: 20px;
        padding-right: 20px;
    }
    
    @include mobile {
        padding-top: 100px;
        max-width: 100%;
        height: auto;
        flex-direction: column-reverse;
        align-items: center;
        padding-left: 16px;
        padding-right: 16px;
    }
}

.tekstil_image {
    flex-shrink: 0;
    
    @include tablet {
        max-width: 698px;
        height: auto;
    }
    
    @include mobile {
        max-width: 100%;
        height: auto;
    }
}

.tekstil_li{
    font-size: var(--text-lg);
    font-family: var(--font-family);
    margin-left: 45px;
    display: flex;
    align-items: flex-start;
    gap: 15px;
    
    @include tablet {
        margin-left: 0;
    }
    
    @include mobile {
        margin-left: 0;
        gap: 12px;
    }
}

a{
    text-decoration: none;
    color: var(--dark-gold);
}

.tekstil_right img{
    margin-left: -45px;
    padding-top: 25px;
    @include tablet {
        margin-left: 0;
    }
}

.tekstil_right{
    margin-left: 160px;
    margin-top: 100px;
    flex: 1;
    
    @include tablet {
        margin-left: 30;
        margin-top: 40px;
        width: 100%;
        padding: 0 10px;
    }
    
    @include mobile {
        margin-left: 0;
        margin-top: 30px;
        width: 100%;
        padding: 0 10px;
    }
}

.tekstil_title{
    font-size: var(--text-2xl);
    font-family: var(--font-family);
    
    @include tablet {
        font-size: 24px;
        text-align: start;
    }
    
    @include mobile {
        font-size: 20px;
        text-align: center;
    }
}

.tekstil_li_title{
    padding-top: 10px;
    word-break: break-word;
    
    @include tablet {
        margin-top: 0;
        font-size: 16px;
    }
    
    @include mobile {
        margin-top: 0;
        font-size: 14px;
    }
}

.tekstil_li_bottom{
    margin-top: 30px;
}

.custom-button {
    width: 300px !important;
    margin-top: 40px;
    
    @include tablet {
        margin-top: 40px;
        margin-bottom: 40px;
    }
    
    @include mobile {
        margin-top: 30px;
        margin-bottom: 30px;
        margin-left: auto;
        margin-right: auto;
        display: flex;
        width: 100% !important;
        max-width: 300px;
    }
}
</style>