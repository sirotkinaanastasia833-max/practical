<script setup lang="ts">
import Logo from '@/components/ui/Logo.vue';
import Emblem from '@/components/header/Emblem.vue';
import Profile from '@/components/header/Profile.vue';
import Number from '@/components/header/Number.vue';
import Navbar from '@/components/header/Navbar.vue';
</script>

<template>
  <header class="header">
    <Logo class="logo"/>
    <Emblem class="emblem"/>
    <p class="title_header">Производитель турецкого<br> трикотажного полотна</p>
  
    <div class="basket"><img src="./../../assets/images/basket.png" alt=""></div>

    <Profile class="profil_header"/>

    <Number/>
    
  </header>
  <Navbar/>
</template>

<style scoped lang="scss">
  .header{
    max-width: 100%;
    max-height: 110px;
    background-color: var(--color-dark-blue);
    display: flex;
    flex-wrap: nowrap;
  }
  .title_header{
    font-size: var(--text-xs);
    font-family: var(--font-family);
    color: var(--text-color);
    margin: 30px 20px 10px 30px;
  }
  .emblem{
    margin: 20px 10px 10px 10px;
  }
  .logo{
    margin: 10px 10px 20px 85px;
  }
  .basket{
    margin: 20px 10px 10px 150px;
  }
  .profil_header{
    margin: 30px 10px 10px 10px;
  }
</style>