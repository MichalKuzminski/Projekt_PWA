<template>
    <div class="footer-info-wrapper">
        <div class="content content-left">
            <slot name="content-left">
                Domyślna wartosc slota
            </slot>
        </div>
        <div @click="scrollToTop()" class="action-buttons">
            <Icon name="ci:caret-up-md" />
        </div>
        <div class="content content-right">
            <slot name="content-right">
                Domyślna wartosc slota
            </slot>

        </div>

    </div>
</template>

<script lang="ts">


import { defineComponent } from 'vue'
export default defineComponent({

    setup() {
        const scrollToTop = (): void => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });

        }

        return {
            scrollToTop
        }
    }
}
)
</script>

<style lang="scss" scoped>
@import '@/globalStyles.scss';

.footer-info-wrapper {
    width: 100%;
    display: flex;
    justify-content: space-between;
    background-color: $header-info-background-color;
    align-items: center;
    height: $bottom-info-height;
    padding-inline: $bottom-info-padding;
    font-size: 12px;

    .content {
        text-align: center;
    }

    .action-buttons {
        position: absolute;
        right: 50%;
        border: 1px solid $bottom-info-border-color;
        border-radius: 10px;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 40px;
        height: 30px;
        transition: all 0.2s;
        font-size: 21px;

        &:hover {
            background-color: rgba($bottom-info-border-color, .4);
        }
    }
}
</style>