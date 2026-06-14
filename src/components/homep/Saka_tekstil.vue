<template>
    <div class="tekstil">
        <img src="./../../assets/images/sakatekstil.png" alt="">
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
</template>

<script>
import Button from '@/components/ui/Button.vue'
export default {
  components: {
    Button
  }
}
</script>

<style>
.tekstil{
    width: 100%;
    height: 639px;
    background-color: var(--saka-color);
    display: flex;
    flex-wrap: nowrap;
}

.tekstil_li{
    font-size: var(--text-lg);
    font-family: var(--font-family);
    margin-left: 45px;
}

a{
    text-decoration: none;
    color: var(--dark-gold);
}

.tekstil_right img{
    margin-left: -45px;
}

.tekstil_right{
    margin-left: 160px;
    margin-top: 100px;
}

.tekstil_title{
    font-size: var(--text-2xl);
    font-family: var(--font-family);
}
.tekstil_li_title{
    margin-top: -18px;
}

.tekstil_li_bottom{
    margin-top: 30px;
}

.custom-button {
    width: 300px !important;
    margin-top: 80px;
}


</style>