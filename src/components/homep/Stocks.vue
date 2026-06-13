<script setup lang="ts">

</script>

<template>
    <div class="stocks_wrapper">
        <div class="skewed-box">
            <span class="stocks_title">АКЦИИ</span>
        </div>
        <div class="stocks_wrapper_fabric">
            <div class="stocks_fabric">
                <img src="./../../assets/images/culinary_fabric.png" alt="" class="stocks_img">
                <span class="stocks_title_fabric">Кулинарная гладь</span>
            </div>
            <div class="stocks_fabric">
                <img src="./../../assets/images/footer.png" alt="" class="stocks_img">
                <span class="stocks_title_fabric">Футер</span>
            </div>
            <div class="stocks_fabric">
                <img src="./../../assets/images/kashkorse.png" alt="" class="stocks_img">
                <span class="stocks_title_fabric">Кашкорсе, рибана</span>
            </div>
            <div class="stocks_fabric">
                <img src="./../../assets/images/pique.png" alt="" class="stocks_img">
                <span class="stocks_title_fabric">Пике</span>
            </div>
            <div class="stocks_fabric">
                <img src="./../../assets/images/interlock.png" alt="" class="stocks_img">
                <span class="stocks_title_fabric">Интерлок</span>
            </div>
            <div class="stocks_fabric">
                <img src="./../../assets/images/kapitonium.png" alt="" class="stocks_img">
                <span class="stocks_title_fabric">Капитоний</span>
            </div>
            <div class="stocks_fabric">
                <img src="./../../assets/images/selanik.png" alt="" class="stocks_img">
                <span class="stocks_title_fabric">Селаник</span>
            </div>
            <div class="stocks_fabric">
                <img src="./../../assets/images/velour.png" alt="" class="stocks_img">
                <span class="stocks_title_fabric">Велюр</span>
            </div>
            <div class="stocks_fabric">
                <img src="./../../assets/images/viscose.png" alt="" class="stocks_img">
                <span class="stocks_title_fabric">Вискоза</span>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.skewed-box {
  width: 140px;
  height: 51px;
  background: var(--yellow-color);
  clip-path: polygon(0% 0%, 100% 0%, 85% 100%, 0% 100%);
  margin: 0px 0px 0px 220px;
}
.stocks_wrapper{
    max-width: 100%;
    max-height: 50px;
    background-color: var(--color-dark-blue);
    display: flex;
    flex-wrap: nowrap;
}
.stocks_wrapper_fabric{
    display: flex;
    flex-wrap: nowrap;
    gap: 23px;
    margin-left: 15px;
}
.stocks_fabric{
    display: flex;
    align-items: center;
}
.stocks_title_fabric{
    margin-left: 7px;
    color: var(--text-color);
    font-family: var(--font-family);
    font-size: var(--text-xxs);
}
.stocks_title{
    display: flex;
    justify-content: center;
    margin: 15px 7px 0px 0px;
    font-family: var(--font-family);
    font-size: var(--text-sm);
    color: var(--text-color-black);
}
</style>