<template>
  <div class="Container">
    <nav class="navbar">
      <div class="nav-container">
          <div class="nav">      
              <router-link to="/" class="nav-link" active-class="active" exact>Главная</router-link>
              <router-link to="/catalog" class="nav-link" active-class="active">Каталог <img src="./../../assets/images/nav.png" alt=""></router-link>
              <router-link to="/about" class="nav-link" active-class="active">О компании</router-link>
              <router-link to="#" class="nav-link" active-class="active">Новости</router-link>
              <router-link to="#" class="nav-link" active-class="active">Доставка и оплата</router-link>
              <router-link to="#" class="nav-link" active-class="active">Контакты</router-link>
          </div>
      </div>
    </nav>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped lang="scss">
.navbar{
    max-width: 100%;
    max-height: 60px;
    background-color: var(--color-nav);
    display: flex;
    flex-wrap: nowrap;
    justify-content: center;
}

.nav-container{
    display: flex;
    flex-wrap: nowrap;
    
}
.nav{
    padding: 15px 0px;
}
.nav-link{
    margin: 0px 62px 0px 62px;
    color: var(--text-color);
    text-decoration: none;
    font-size: var(--text-sm);
    font-family: var(--font-family);
}
</style>