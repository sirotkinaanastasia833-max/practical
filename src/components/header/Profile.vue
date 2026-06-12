<template>
    <div class="profile_wrapper">
        <div class="image_profile"><img src="./../../assets/images/User.png" alt=""></div>
        <span class="profile_title">Войти</span>
    </div>
</template>

<script>
</script>

<style scoped lang="scss">
    .profile_title{
        font-size: var(--text-xs);
        font-family: var(--font-family);
        color: var(--text-color);
    }
    .image_profile{
        margin: 1px 7px 0px 0px;
    }
    .profile_wrapper{
        display: flex;
        flex-wrap: nowrap;
    }
</style>