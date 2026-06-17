<script setup lang="ts">
import Logo from '@/components/ui/Logo.vue';
import Emblem from '@/components/header/Emblem.vue';
import Profile from '@/components/header/Profile.vue';
import Number from '@/components/header/Number.vue';
import Navbar from '@/components/header/Navbar.vue';
</script>

<template>
  <div class="Container">
    <header class="header">
      <Logo class="logo"/>
      <Emblem class="emblem"/>
      <p class="title_header">Производитель турецкого<br> трикотажного полотна</p>
      
      <div class="basket"><img src="./../../assets/images/basket.png" alt=""></div>

      <Profile class="profil_header"/>

      <Number class="number"/>
      
    </header>
    <Navbar class="navbar"/>
  </div>
</template>

<style scoped lang="scss">
@use '@/assets/styles/mixins.scss' as *;
  .header{
    max-width: 100%;
    max-height: 110px;
    background-color: var(--color-dark-blue);
    display: flex;
    flex-wrap: nowrap;
    justify-content: center;
    @include tablet {
       justify-content: start;
    }
  }
  .title_header{
    font-size: var(--text-xs);
    font-family: var(--font-family);
    color: var(--text-color);
    margin: 30px 20px 10px 30px;
    @include tablet {
       display: none;
    }
  }
  .emblem{
    margin: 20px 10px 10px 10px;
  }
  .logo{
    display: flex;
    justify-content: center;
    @include tablet {
      margin: 10px 10px 20px 50px;
    }
  }
  .basket{
    margin: 20px 10px 10px 150px;
    @include tablet {
       display: none;
    }
  }
  .profil_header{
    margin: 30px 10px 10px 10px;
    @include tablet {
       display: none;
    }
  }
  .number{
    @include tablet {
       display: none;
    }
  }
  .navbar{
    @include tablet {
       display: none;
    }
  }
</style>