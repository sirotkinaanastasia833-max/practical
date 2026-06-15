<script setup lang="ts">

defineProps<{
    text?: string
    theme?: 'full' | 'icon' | 'text'
    transform?: string
    icon?: string
}>()

</script>

<!-- <template>
    <button class="'btn-${{theme}}'">
        <span v-if="theme !== 'icon'" >{{ text }}</span>
        <img v-if="theme === 'icon' || theme === 'full'"
        :src="icon"
        alt="">
    </button>
</template> -->

<template>
    <button class="btn" :class="`btn--${theme}`">
    <span v-if="theme !== 'icon'" class="btn__text">
        {{ text }}
    </span>

    <img
        v-if="theme === 'icon' || theme === 'full'"
        class="btn__icon"
        :src="icon"
        alt=""
    >
    </button>
</template>

<style scoped lang="scss">
@use '@/assets/styles/variables.scss' as *;
    .btn {
        border: none;
        cursor: pointer;
        font-family: inherit;

        display: inline-flex;
        align-items: center;
        justify-content: center;

        background-color: var(--dark-gold);
        color: var(--text-color-black);

        &__text {
            font-size: var(--text-base);
            font-weight: 700;
            line-height: 1;
            font-family: var(--font-family);
        }

        &__icon {
            width: 15px;
            height: 15px;
            object-fit: contain;
        }

        &--icon {
            width: 50px;
            height: 50px;
            padding: 0;
            border-radius: 50%;
        }

        &--full {
            width: 260px;
            height: 60px;
            padding: 0 52px;
            border-radius: 100px;

            justify-content: space-between;
            gap: 67px;
        }

        &--text {
            width: auto;
            max-width: 180px;
            height: 32px;
            padding: 0 18px;
            border-radius: 30px;
            background-color: var(--dark-gold);
            color: var(--text-color-black);
            justify-content: center;
            text-align: center;

            .btn__text {
                font-size: var(--text-sm);
                font-weight: 500;
                line-height: 1;
                font-family: var(--font-family);
            }
        }
    }
</style>


