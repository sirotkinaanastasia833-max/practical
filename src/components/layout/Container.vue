<template>
    <div class="container">
        <slot />
    </div>
</template>

<script setup lang="ts">

</script>

<style lang="scss" scoped>
.container {
    max-width: 1200px;
    margin: 0 auto;
    

    @include tablet {
        max-width: 960px;
    }

    @include mobile {
        max-width: 480px;
    }
}
</style>