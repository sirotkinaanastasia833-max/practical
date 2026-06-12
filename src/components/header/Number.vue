<template>
    <div class="container_number">
        <div class="number_wrapper">
            <div><img src="./../../assets/images/Phone.png" alt="" class="number_image"></div>
            <span class="telephone">+90 212 547 08 26</span>
        </div>
        <a href="#" class="link">Заказать звонок</a>
    </div>
    
</template>

<script>
</script>

<style scoped lang="scss">
    .number_wrapper{
        display: flex;
        flex-wrap: nowrap;
    }
    .number_image{
        margin-top: 30px;
    }
    .container_number{
        display: grid;
        grid-template-columns: 1fr;
        margin-left: 30px;
    }
    .telephone{
        margin-top: 30px;
        color: var(--text-color);
        font-size: var(--text-xl);
    }
    .link{
        margin: -20px 0px 0px 75px;
        font-size: var(--text-xs);
        color: var(--text-color);
        font-family: var(--font-family);
    }
</style>